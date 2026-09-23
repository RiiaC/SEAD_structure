---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity analysis_entity.md
created: 2026-09-15T10:31:11.659Z
modified: 2026-09-23T05:19:01.151Z
published: 2026-09-23T05:19:01.151Z
Entity_Name: analysis_entity
Type: Data (Derived)
Source_entity: "[[Entity supersite|Entity supersite]]"
Public_ID: "[[analysis_entity_id]]"
columns:
  - "[[physical_sample_key]]"
  - "[[unique_row_identifer]]"
Target_Entity: "[[Entity dataset|Entity dataset]]"
Local_Keys:
  - "[[dataset_name]]"
Remote_Keys:
  - "[[dataset_name]]"
SEAD_table: "[[tbl_analysis_entities]]"
status: complete
Target_Entity_2: "[[Entity sample]]"
Local_Keys_2: "[[physical_sample_key]]"
Remote_Keys_2: "[[physical_sample_key]]"
change_it: true
---

> [!info]  The table that records what is actually analysed.
> In this dataset, perhaps we can simply attach an analysis\_entities\_id to every row by `labnr` and call it good?

![[images/Entity analysis_entities schema.png]]

# YAML as of 2026-09-17

````
name: analysis_entity
type: entity
system_id: system_id
keys:
  - unique_row_identifier
  - lab_id
columns:
  - unique_row_identifier
  - physical_sample_key
public_id: analysis_entity_id
source: supersite
foreign_keys:
  - entity: dataset
    local_keys:
      - dataset_name
    remote_keys:
      - dataset_name
    how: inner
    constraints:
      cardinality: one_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
  - entity: sample
    local_keys:
      - physical_sample_key
    remote_keys:
      - physical_sample_key
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: false
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
drop_duplicates: true
check_functional_dependency: false
extra_columns:
  dataset_name: Strucke C14
```
````
