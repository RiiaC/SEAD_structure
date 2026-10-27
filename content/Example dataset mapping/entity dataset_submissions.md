---
publish: true
permalink: /Example dataset mapping/entity dataset_submissions.md
created: 2026-10-27T14:48:44.731Z
modified: 2026-10-27T14:59:59.741Z
published: 2026-10-27T14:59:59.741Z
Entity_Name: dataset_submissions
Type:
Source_entity:
Public_ID:
columns:
Target_Entity:
Local_Keys: []
Remote_Keys:
SEAD_table: "[[tbl_dataset_submisssions]]"
status:
---

> [!info] This is one of the metadata tables needed for this project

- [ ] finish filling this in--add info on submission type and connect this table to the other metadata tables

# YAML as of 2026-10-27

````
name: dataset_submissions
type: fixed
system_id: system_id
keys: []
columns:
  - date_submitted
  - notes
  - dataset_id
  - sumbission_type_id
  - contact_id
public_id: dataset_submission_id
values:
  - - 1
    - null
    - '2026-08-12'
    - https://zenodo.org/records/21932353
    - null
    - null
    - null
```
````
