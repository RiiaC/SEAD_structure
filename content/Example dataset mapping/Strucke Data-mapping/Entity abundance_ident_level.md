---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity abundance_ident_level.md
modified: 2026-09-17T10:30:14.307Z
---

> [!info] This one exists to make it possible to record the question mark (identification level 1) that sometimes appears next to a species name

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
