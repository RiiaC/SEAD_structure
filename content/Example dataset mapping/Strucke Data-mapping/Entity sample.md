---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity sample.md
modified: 2026-09-21T05:21:41.679Z
---

> [!info] links the samples with sample group names as defined in the [[Entity supersite]] entity

![[images/Entity physical_samples schema.png]]

# YAML as of 2026-08-25

````
name: sample
type: entity
system_id: system_id
keys: []
columns:
  - physical_sample_key
  - sample_group_key
  - lab_id
public_id: physical_sample_id
source: supersite
foreign_keys:
  - entity: sample_group
    local_keys:
      - sample_group_key
    remote_keys:
      - sample_group_key
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: false
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
drop_duplicates: true
check_functional_dependency: false
drop_empty_rows: true
```
````
