---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/Entity feature_types.md
---

> [!info] The Strucke column `context_type` seems to equate to SEADs `tbl_feature_types`
> However the ones in the Strucke dataset are in Swedish, while the ones in SEAD are in English. We will need to determine which ones are already in SEAD (what their `feature_type_id`is, or if they need a new one), and if there are any issues with spelling that result in more than one `context_type` in the Strucke that clearly are describing the same type of context (like we see in the species column).
> I suspect that we will want to preserve the Swedish word, too, in another column (possibly the [[Structure of SEAD/Columns/description|description]] column of [[tbl_features]]) but that is a discussion we can have with Phil when he returns.

- [x] create entity
- [ ] look up what Bruno has accomplished with this part (https://github.com/Br1CM/sead\_strucke\_data\_cleaning/tree/split-archive-current-pipeline)
- [ ] figure out what to do next

![[images/Entity feature_types schema.png]]

# YAML as of 2026-08-25

````
name: feature_types
type: entity
system_id: system_id
keys: []
columns:
  - anlaggning
  - anlnr
  - fid
public_id: feature_type_id
source: datasheet_v9
drop_duplicates:
  - anlaggning
check_functional_dependency: false
drop_empty_rows:
  - anlaggning

```
````
