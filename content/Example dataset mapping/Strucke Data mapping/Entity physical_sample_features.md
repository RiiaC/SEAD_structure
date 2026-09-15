---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/Entity physical_sample_features.md
---

> [!info] this table links the features and the physical samples
>
> >

- [x] create entity
- [x] join to both of the other tables

![[images/Entity physical_sample_features schema.png]]

# YAML as of 2026-08-25

````
name: physical_sample_features
type: entity
system_id: system_id
keys: []
columns:
  - fid
  - context_id
  - context_type
public_id: physical_sample_feature_id
source: datasheet_v9
foreign_keys:
  - entity: physical_samples
    local_keys:
      - fid
    remote_keys:
      - fid
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
  - entity: features
    local_keys:
      - fid
    remote_keys:
      - fid
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true

```
````
