---
publish: true
permalink: /Example dataset mapping/AFL Radiocarbon Data mapping/Entity modification_types.md
created: 2026-07-24T09:34:07.989Z
modified: 2026-09-23T05:19:00.132Z
published: 2026-09-23T05:19:00.132Z
Entity_Name: modification_types
Type: Fixed Values
Public_ID: "[[modification_type_id]]"
Target_Entity:
Local_Keys:
  - 
  - 
  - 
Remote_Keys:
SEAD_table: "[[tbl_modification_types]]"
status:
change_it: true
---

> [!info] the table into which we will put the info from [[C. Biological Age]]

- [x] create fixed-value table for the modification types used in this dataset, and enter the following:

| modification\_type\_id | modification\_type\_name | modification\_type\_description         |
| -------------------- | ---------------------- | ------------------------------------- |
|                      | nd                     | The estimated biological age at death |
|                      | 0-3 m                  | The estimated biological age at death |
|                      | 3-10 m                 | The estimated biological age at death |
|                      | neonat                 | The estimated biological age at death |
|                      | juvenile               | The estimated biological age at death |
|                      | subadult               | The estimated biological age at death |
|                      | adult                  | The estimated biological age at death |

![[images/Entity modification_types schema.png]]
