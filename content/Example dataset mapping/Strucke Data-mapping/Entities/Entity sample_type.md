---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entities/Entity sample_type.md
created: 2026-11-03T13:45:44.167Z
modified: 2026-11-04T13:32:32.473Z
published: 2026-11-04T13:32:32.473Z
Entity_Name: sample_type
Type: Fixed Values
Public_ID: sample_type_id
columns:
Target_Entity:
Local_Keys: []
Remote_Keys:
SEAD_table: "[[tbl_sample_types]]"
status:
---

> [!info] We need to assign a sample type to each row in the dataset.
>
> - Those that have more than one species will be assigned to the existing [[sample_type_id]] = 14 = Dating pseudosample
> - Those with only one species will be assigned a new [[sample_type_id]] number for "Dating Sample"
> - [ ] figure out how to make this split work automatically

# YAML as of 2026-11-04

````
name: sample_type
type: fixed
system_id: system_id
keys: []
columns:
  - type_name
  - description
public_id: sample_type_id
values:
  - - 1
    - null
    - Dating pseudosample
    - Virtual sample consisting of aggregated material from multiple samples to bulk up weight for radiocarbon dating (or other dating method)
  - - 2
    - null
    - Dating sample
    - A sample analysed for radiocarbon dating (or other dating method)
```
````
