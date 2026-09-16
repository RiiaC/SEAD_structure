---
publish: true
permalink: /Example dataset mapping/Strucke datamapping with Brunos code/Entity methods.md
---

> [!info] these are all radiocarbon dates

- [x] create the entity
- [ ] determine which method from the list at [[tbl_methods#3. Dating by radiometric methods]]  is the best match for this data set.
  In the meantime, going with **148**  = **Radiocarbon (14C Unspecified)**

Use Burno's entity methods, which has sql to query SEAD for methods  (which is not working as of 2026-09-11, message sent to Roger about it)

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
