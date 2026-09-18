---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity language.md
modified: 2026-09-18T13:14:46.541Z
---

> [!info] most of the common names in the list of species for this data set are in Swedish, which has language\_id = 2 in SEAD
> Bruno created this one, but doesn't appear to have finished it, as he didn't enter any values
>
> - [ ] Figure out how best to attach `language_id` = 2 to all rows in the dataset with a Swedish common name listed for species.

![[Pasted image 20260918151342.png|600]]

# YAML as of 2026-09-18

````
name: language
type: fixed
system_id: system_id
keys:
  - language_name_english
columns:
  - system_id
  - language_id
  - language_name_english
  - language_name_native
public_id: language_id
values:
  - - 1
    - null
    - null
    - null
  - - 2
    - null
    - null
    - null
```
````
