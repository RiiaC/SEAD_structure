---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/Entity features.md
---

> [!info] the column context\_id contains the name of the archaeological feature that was sampled for this analysis

- [x] create entity
- [x] join to [[Entity feature_types]]
  ![[images/Entity features schema.png]]

# YAML as of 2026-08-25

````
name: features
type: entity
system_id: system_id
keys: []
columns:
  - fid
  - context_id
  - context_type
public_id: feature_id
source: datasheet_v9
foreign_keys:
  - entity: feature_types
    local_keys:
      - context_id
    remote_keys:
      - context_id
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
drop_empty_rows:
  - anlaggning

```
````
