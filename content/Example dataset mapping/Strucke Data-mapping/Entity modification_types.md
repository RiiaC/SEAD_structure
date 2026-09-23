---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity modification_types.md
created: 2026-09-15T10:31:11.778Z
modified: 2026-09-23T05:19:01.433Z
published: 2026-09-23T05:19:01.433Z
Entity_Name: modification_types
Type: Data (Derived)
Source_entity: "[[Entity superabundance]]"
Public_ID: "[[modification_type_id]]"
columns:
  - "[[modification_type]]"
Target_Entity:
Local_Keys: []
Remote_Keys:
SEAD_table: "[[tbl_modification_types]]"
status: outstanding_question
change_it: true
---

- [ ] I think we should also add a [[modification_type_description]], do the others agree?

> [!info] The "material" column of the Strucke data sometimes has additional information in the cell which would fall under [[tbl_abundance_modifications]]:
>
> - (ej förkolnat)
> - brända
> - obrända
> - obränt
>   this information will need to be extracted from this column before data ingestion. None of these are already in SEAD (see [[tbl_modification_types]]), so they will all get new [[modification_type_id]] as well as [[abundance_modification_id]] numbers

- [x] create a fixed-values entity for modification types
- [x] add columns for [[modification_type_name]] and [[modification_type_description]]
- [x] fill in the fixed values for them as follows:

| [[modification_type_id]] | [[modification_type_name]] | [[modification_type_description]]                                                                                    |
| ------------------------ | -------------------------- | -------------------------------------------------------------------------------------------------------------------- |
|                          | brända                     | used when the material analysed was burned                                                                           |
|                          | obrända                    | used when the material analysed was not burned  (presumably noted as such because most material in that project was) |
|                          | obränt                     | used when the material analysed was not burned  (presumably noted as such because most material in that project was) |
|                          | förkolnat                  | used when the material analysed was charred                                                                          |
|                          | ej förkolnat               | used when the material analysed is not charred (presumably noted as such because most material in that project was)  |

![[images/abundance_modifications schema.png]]

# YAML as of 2026-09-21

````
name: modification_type
type: entity
system_id: system_id
keys: []
columns:
  - modification_type
public_id: modification_type_id
source: superabundance
drop_duplicates: true
check_functional_dependency: false
drop_empty_rows: true
```
````
