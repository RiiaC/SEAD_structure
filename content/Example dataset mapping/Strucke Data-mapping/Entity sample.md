---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity sample.md
created: 2026-09-17T15:32:52.387Z
modified: 2026-09-24T05:44:37.395Z
published: 2026-09-24T05:44:37.395Z
Entity_Name: physical_samples
Type: Data (Derived)
Source_entity: "[[Entity supersite|Entity supersite]]"
Public_ID: "[[physical_sample_id]]"
columns:
  - "[[lab_id]]"
  - "[[physical_sample_key]]"
  - "[[sample_group_key]]"
Target_Entity: "[[Entity sample_group]]"
Local_Keys:
  - "[[sample_group_key]]"
Remote_Keys:
  - "[[sample_group_key]]"
SEAD_table: "[[tbl_physical_samples]]"
status: complete
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
