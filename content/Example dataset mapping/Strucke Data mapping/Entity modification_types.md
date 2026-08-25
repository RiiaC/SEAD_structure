---
Entity_Name: modification_types
Type: Fixed Values
Public_ID: "[[modification_type_id]]"
Target_Entity:
Local_Keys:
  - 
  - 
  - 
Remote_Keys:
SEAD_table: "[[tbl_modification_types]]"
status: complete
publish: true
---
> [!info] The "material" column of the Strucke data sometimes has additional information in the cell which would fall under [[tbl_abundance_modifications]]:
> - (ej förkolnat)
> - brända
> - obrända
> - obränt
   this information will need to be extracted from this column before data ingestion. None of these are already in SEAD (see [[tbl_modification_types]]), so they will all get new [[modification_type_id]] as well as [[abundance_modification_id]] numbers


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


![[abundance_modifications schema.png]]



# YAML as of 2026-08-25
````
name: modification_types
type: fixed
system_id: system_id
keys: []
columns:
  - system_id
  - modification_type_id
  - modification_type_name
  - modification_type_description
public_id: modification_type_id
values:
  - - 1
    - null
    - null
    - null
  - - 2
    - null
    - null
    - null
  - - 3
    - null
    - null
    - null
  - - 4
    - null
    - null
    - null
  - - 5
    - null
    - null
    - null

```
