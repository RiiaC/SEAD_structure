---
Entity_Name: abundances
Type: Data (Derived)
Public_ID: "[[abundance_id]]"
Target_Entity: "[[Example dataset mapping/Strucke Data mapping/Entity analysis_entities|Entity analysis_entities]]"
Local_Keys:
  - lab_no
Remote_Keys: lab_no
SEAD_table: "[[tbl_abundances]]"
status: in progress
publish: true
---
> [!info] we don't have counts of the things that were dated, but we do know that at least one something had to be present to have been dated, 
> and in SEAD it is the abundances table that become an analysis entity, which in turn has analysis values and/or geochronological results.  Therefore, we need this entity, too.

- [x] create a data-derived entity for abundances
- [x] select `labno`, `species
- [x] add an extra column, [[abundance]] and give it always a value of 1, now we have "counted" one for each row
- [x] join this to [[Example dataset mapping/Strucke Data mapping/Entity abundance_modifications|Entity abundance_modifications]] om `lab_no`



![[Entity abundances schema 1.png]]



# YAML as of 2026-08-25
````
name: abundances
type: entity
system_id: system_id
keys: []
columns:
  - species
  - lab_id
  - fid
public_id: abundance_id
source: datasheet_v9
foreign_keys:
  - entity: analysis_entities
    local_keys:
      - lab_no
    remote_keys:
      - lab_no
    how: inner
    constraints:
      cardinality: one_to_many
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
      allow_null_keys: false
      allow_unmatched_left: true
extra_columns:
  abundance: '1'
`````
