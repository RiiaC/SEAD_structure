---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity analysis_entity.md
modified: 2026-09-21T05:14:04.011Z
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
