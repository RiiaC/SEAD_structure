---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity identification_level.md
modified: 2026-09-18T13:09:50.246Z
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
