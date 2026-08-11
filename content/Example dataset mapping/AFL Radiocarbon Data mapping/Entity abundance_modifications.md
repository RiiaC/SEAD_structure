---
Entity_Name: abundance_modifications
Type: Data (Derived)
Public_ID: "[[abundance_modification_id]]"
Target_Entity: "[[Entity modification_types]]"
Local_Keys:
  - biological_age
Remote_Keys:
  - "[[modification_type_name]]"
SEAD_table: "[[tbl_abundance_modifications]]"
status: error_to_solve
publish: true
---
> [!info] the table Tom suggested, on 2026-02-19, to use for the [[C. Biological Age]], as it is a characteristic of the bone being sampled


- [x] create a data-derived entity for abundance_modifications, and add the column biological_age
- [ ] join it to the [[Entity modification_types]] where biological age = modification_type_name *(this attempted 2026-04-22, but ran into errors--Roger is looking into them)*

![[Entity abundance_modifications schema.png]]

# YAML

````
name: abundance_modifications
type: entity
system_id: system_id
keys: []
columns:
  - lab_nr
  - biological_age
public_id: abundance_modification_id
source: datasheet
foreign_keys:
  - entity: modification_types
    local_keys:
      - biological_age
    remote_keys:
      - modification_type_name
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
      allow_null_keys: false
drop_empty_rows:
  - biological_age
`````


