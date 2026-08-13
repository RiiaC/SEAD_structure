---
Entity_Name: abundance_modifications
Type: Data (Derived)
Public_ID: "[[abundance_modification_id]]"
Target_Entity: "[[Example dataset mapping/Strucke Data mapping/Entity modification_types|Entity modification_types]]"
Local_Keys:
  - "[[modification_type_name]]"
Remote_Keys:
  - "[[modification_type_name]]"
SEAD_table: "[[tbl_abundance_modifications]]"
status: complete
publish: true
---
> [!info] The "material" column of the Strucke data sometimes has additional information in the cell which would fall under [[tbl_abundance_modifications]]:
> - (ej förkolnat)
> - brända
> - obrända
> - obränt
   this information will need to be extracted from this column before data ingestion. None of these are already in SEAD (see [[tbl_modification_types]]), so they will all get new [[modification_type_id]] as well as [[abundance_modification_id]] numbers

- [x] create entity `anundance_modifications` and fill it with the material column from the dataset
- [ ] add an extra column `modification_type_name` and paste this code into the Expression box:
````
=coalesce(regex_extract(lower(trim(material)), 'obrända|obränt|brända|(ej förkolnat)|förkolnat'),  '' )
````
- [x] create a Foreign key connecting this table to [[Example dataset mapping/Strucke Data mapping/Entity modification_types|Entity modification_types]] on the foreign key [[modification_type_name]]

# schema image

![[abundance_modifications schema.png|500]]

# YAML as of 2026-08-12
````
name: abundance_modifications
type: entity
keys: []
columns:
  - material
public_id: abundance_modification_id
source: datasheet
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
extra_columns:
  modification_type_name: '=coalesce(regex_extract(lower(trim(material)), ''obrända|obränt|brända|(ej förkolnat)|förkolnat''),  '''' )'

```