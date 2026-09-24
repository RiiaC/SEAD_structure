---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity sample_feature.md
created: 2026-09-21T05:22:14.834Z
modified: 2026-09-24T05:44:37.395Z
published: 2026-09-24T05:44:37.395Z
Entity_Name: sample_feature
Type: Data (Derived)
Source_entity: "[[Entity supersite|Entity supersite]]"
Public_ID: "[[physical_sample_feature_id]]"
columns:
  - "[[lab_id]]"
  - "[[physical_sample_key]]"
  - "[[unique_row_identifer]]"
Target_Entity: "[[Entity sample]]"
Local_Keys:
  - "[[physical_sample_key]]"
Remote_Keys:
  - "[[physical_sample_key]]"
SEAD_table: "[[tbl_physical_sample_features]]"
status: complete
Target_Entity_2: "[[Entity feature]]"
Local_Keys_2: "[[unique_row_identifer]]"
Remote_Keys_2: "[[unique_row_identifer]]"
---

> [!info] uses info from [[Entity supersite]] to create the joins

# YAML as of 2026-09-21

````
name: sample_feature
type: entity
system_id: system_id
keys:
  - lab_id
  - unique_row_identifier
columns:
  - lab_id
  - unique_row_identifier
  - physical_sample_key
public_id: physical_sample_feature_id
source: supersite
foreign_keys:
  - entity: sample
    local_keys:
      - physical_sample_key
    remote_keys:
      - physical_sample_key
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
  - entity: feature
    local_keys:
      - unique_row_identifier
    remote_keys:
      - unique_row_identifier
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
drop_duplicates: true
check_functional_dependency: false
drop_empty_rows: true
```
````
