---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity method.md
created: 2026-09-15T10:31:11.770Z
modified: 2026-09-24T05:44:37.366Z
published: 2026-09-24T05:44:37.366Z
Entity_Name: method
Type: SQL query
Source_entity: SEAD
Public_ID: "[[method_id]]"
Target_Entity:
Local_Keys: []
Remote_Keys:
SEAD_table: "[[tbl_methods]]"
status: outstanding_question
---

> [!info] these are all radiocarbon dates. I am not clear why Bruno has this sql looking for all methods in SEAD

- [x] create the entity

- [ ] determine which method from the list at [[tbl_methods#3. Dating by radiometric methods]]  is the best match for this data set.
  In the meantime, going with **148**  = **Radiocarbon (14C Unspecified)**

- [ ] Use Burno's entity methods, which has sql to query SEAD for methods or just do a fixed values entity, and assign the right one?

# YAML as of 2026-08-25

````
name: methods
type: entity
system_id: system_id
keys: []
columns:
  - fid
public_id: method_id
source: datasheet_v9
extra_columns:
  method: 39

```
````
