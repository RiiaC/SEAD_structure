---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity sample_group.md
created: 2026-09-21T05:17:11.019Z
modified: 2026-09-23T05:19:01.416Z
published: 2026-09-23T05:19:01.416Z
Entity_Name: sample_group
Type: Data (Derived)
Source_entity: "[[Entity supersite|Entity supersite]]"
Public_ID: sample_group_id
columns:
  - "[[context_id]]"
  - "[[context_type]]"
  - "[[sample_group_key]]"
  - "[[site_key]]"
Target_Entity: "[[Example dataset mapping/Strucke Data-mapping/Entity site|Entity site]]"
Local_Keys:
  - "[[site_key]]"
Remote_Keys:
  - "[[site_key]]"
SEAD_table: "[[tbl_sample_groups]]"
status: complete
change_it: true
---

> [!info] tells SEAD which site each sample group comes from

# YAML as of 2026-09-21

````
name: sample_group
type: entity
system_id: system_id
keys: []
columns:
  - context_id
  - context_type
  - site_key
  - sample_group_key
public_id: sample_group_id
source: supersite
foreign_keys:
  - entity: site
    local_keys:
      - site_key
    remote_keys:
      - site_key
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
      allow_unmatched_left: true
drop_duplicates: true
check_functional_dependency: false
```
````
