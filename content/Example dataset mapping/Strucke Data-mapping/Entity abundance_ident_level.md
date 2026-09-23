---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity abundance_ident_level.md
created: 2026-09-17T06:04:01.507Z
modified: 2026-09-23T09:18:12.032Z
published: 2026-09-23T09:18:12.032Z
Entity_Name: abundance_ident_level
Type: Data (Derived)
Source_entity: "[[Entity superabundance|Entity superabundance]]"
Public_ID: abundance_ident_level_id
columns:
  - "[[abundance_key]]"
  - "[[material]]"
  - "[[species]]"
Target_Entity: "[[Entity identification_level]]"
Local_Keys:
  - "[[identification_name]]"
Remote_Keys:
  - "[[identification_level_name]]"
SEAD_table: "[[tbl_identification_levels]]"
status: complete
Target_Entity_2: "[[Entity abundance]]"
Local_Keys_2: "[[abundance_key]]"
Remote_Keys_2: "[[abundance_key]]"
change_it: true
extra_columns:
  - "[[identification_name]]"
---

> [!info] This one exists to make it possible to record the question mark that sometimes appears next to a species name, giving them:
>
> - [[identification_level_id]] = 1
> - [[identification_name]] = ?

# YAML as of 2026-09-17

````
name: abundance_ident_level
type: entity
system_id: system_id
keys: []
columns:
  - abundance_key
  - species
  - material
public_id: abundance_ident_level_id
source: superabundance
foreign_keys:
  - entity: identification_level
    local_keys:
      - identification_name
    remote_keys:
      - identification_level_name
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: false
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
  - entity: abundance
    local_keys:
      - abundance_key
    remote_keys:
      - abundance_key
    how: left
    constraints:
      cardinality: one_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
      allow_unmatched_left: true
drop_empty_rows:
  - species
filters:
  - type: query
    query: species.str.contains('?', regex=False, na=False)
extra_columns:
  identification_name: '?'
```
````
