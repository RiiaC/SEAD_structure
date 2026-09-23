---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity physical_sample_features.md
created: 2026-09-15T10:31:11.786Z
modified: 2026-09-23T05:19:01.350Z
published: 2026-09-23T05:19:01.350Z
Entity_Name: physical_sample_features
Type:
Public_ID: "[[physical_sample_feature_id]]"
Target_Entity: "[[Entity sample|Entity sample]]"
Local_Keys:
  - fid
Remote_Keys:
  - fid
SEAD_table: "[[tbl_physical_sample_features]]"
status: is this needed
change_it: true
---

> [!info] this table links the features and the physical samples
>
> >

- [ ] add one to the new shape shifter project?

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
