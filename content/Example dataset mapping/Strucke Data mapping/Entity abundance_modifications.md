---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/Entity abundance_modifications.md
---

> [!info] The "material" column of the Strucke data sometimes has additional information in the cell which would fall under [[tbl_abundance_modifications]]:
>
> - (ej förkolnat)
> - brända
> - obrända
> - obränt
>   this information will need to be extracted from this column before data ingestion. None of these are already in SEAD (see [[tbl_modification_types]]), so they will all get new [[modification_type_id]] as well as [[abundance_modification_id]] numbers

- [x] create entity `anundance_modifications` and the material and species columns from the dataset
- [x] add an extra column `modification_type_name` and paste this code into the Expression box:

```
=coalesce(regex_extract(lower(trim(material)), 'obrända|obränt|brända|(ej förkolnat)|förkolnat'),  '' )
```

- [x] create a Foreign key connecting this table to [[Example dataset mapping/Strucke Data mapping/Entity modification_types|Entity modification_types]] on the foreign key [[modification_type_name]]
- [x] since I had also added two columns for "edited material" and "modification" to the v9 incoming dataset, also add those columns to this entity, to permit a quick visual check to see how that code did.
- [ ] create a Foreign key connecting this entity to [[Example dataset mapping/Strucke Data mapping/Entity abundances|Entity abundances]] on the key "species"
  - [ ] figure out why this one is failing

# schema image

![[images/abundance_modifications schema.png|500]]

# YAML as of 2026-08-25

````
name: abundance_modifications
type: entity
system_id: system_id
keys: []
columns:
  - material
  - material_edited
  - modifacation
  - species
  - fid
public_id: abundance_modification_id
source: datasheet_v9
foreign_keys:
  - entity: modification_types
    local_keys:
      - modification_type_name
    remote_keys:
      - modification_type_name
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
  - entity: abundances
    local_keys:
      - species
    remote_keys:
      - species
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
extra_columns:
  modification_type_name: '=coalesce(regex_extract(lower(trim(material)), ''obrända|obränt|brända|(ej förkolnat)|förkolnat''),  '''' )'

```
````
