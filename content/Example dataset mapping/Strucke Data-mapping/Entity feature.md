---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity feature.md
modified: 2026-09-21T04:56:33.534Z
---

> [!info] This entity tells SEAD that the [[context_id]] of this dataset is the same things as [[feature_name]], and links each named feature of the dataset to the appropriate type of feature based on the [[context_type]] column

![[images/Entity features schema.png]]

# YAML as of 2026-09-18

````
name: feature
type: entity
system_id: system_id
keys:
  - unique_row_identifier
columns:
  - context_type
  - unique_row_identifier
  - context_id
public_id: feature_id
source: datasheet
foreign_keys:
  - entity: feature_type
    local_keys:
      - context_type
    remote_keys:
      - context_type
    how: left
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
      allow_unmatched_left: true
      allow_null_keys: true
drop_duplicates: true
check_functional_dependency: false
drop_empty_rows:
  - context_type
  - context_id
extra_columns:
  feature_name: '{context_id}'
```
````
