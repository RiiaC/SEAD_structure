---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity identification_level.md
created: 2026-09-17T06:25:00.750Z
modified: 2026-09-23T05:19:01.284Z
published: 2026-09-23T05:19:01.284Z
Entity_Name: identification_level
Type: Fixed Values
Public_ID:
columns:
  - "[[identification_level_name]]"
  - "[[indentification_level_abbrev]]"
  - "[[notes]]"
SEAD_table: "[[tbl_identification_levels]]"
status: outstanding_question
change_it: true
---

> [!info] some of the species in this dataset are marked with a question mark,
> so entity is necessary to record an [[identification_level_id]], which Bruno set to 1
>
> - [ ] talk to someone who understands biology conventions, to see if this is correct

# YAML as of 2026-09-17

````
name: identification_level
type: fixed
system_id: system_id
keys: []
columns:
  - system_id
  - identification_level_id
  - identification_level_abbrev
  - identification_level_name
  - notes
public_id: identification_level_id
values:
  - - 1
    - null
    - '?'
    - '?'
    - Uncertainty at ...
```
````
