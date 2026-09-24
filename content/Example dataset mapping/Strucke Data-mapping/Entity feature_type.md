---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity feature_type.md
created: 2026-09-15T10:31:11.718Z
modified: 2026-09-24T05:44:37.309Z
published: 2026-09-24T05:44:37.309Z
Entity_Name: feature_type
Type: Data (Derived)
Source_entity: "[[Entity dataset]]"
Public_ID: "[[feature_type_id]]"
columns:
  - "[[context_type]]"
  - "[[feature_type_name]]"
SEAD_table: "[[tbl_feature_types]]"
status: outstanding_question
---

> [!info] This entity tells Shape Shifter that Strucke column `context_type` is SEAD's [[feature_type_name]]
>
> However the ones in the Strucke dataset are in Swedish, while the ones in SEAD are in English. We will need to determine which ones are already in SEAD (what their `feature_type_id`is, or if they need a new one), and if there are any issues with spelling that result in more than one `context_type` in the Strucke that clearly are describing the same type of context (like we see in the species column).
> I suspect that we will want to preserve the Swedish word, too, in another column (possibly the [[Structure of SEAD/Columns/description|description]] column of [[tbl_features]]) but that is a discussion we can have with Phil when he returns.

- [x] create entity
- [ ] look up what Bruno has accomplished with this part (https://github.com/Br1CM/sead\_strucke\_data\_cleaning/tree/split-archive-current-pipeline)
- [ ] figure out what to do next

![[images/Entity feature_types schema.png]]

# YAML as of 2026-09-18

````
name: feature_type
type: entity
system_id: system_id
keys:
  - context_type
columns:
  - context_type
public_id: feature_type_id
source: datasheet
drop_duplicates: true
check_functional_dependency: false
drop_empty_rows: true
extra_columns:
  feature_type_name: '{context_type}'
```
````
