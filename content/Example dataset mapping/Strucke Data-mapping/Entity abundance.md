---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity abundance.md
modified: 2026-09-17T14:59:59.254Z
---

> [!info] we don't have reported counts for the various bits of plants and animals that were dated in the many projects that comprise this dataset,
> but we do know that at least one something had to be present to have been dated. In SEAD it is the [[tbl_abundances]] (the plant or animal that was counted) that is linked to the [[tbl_analysis_entities]], which in turn has analysis values and/or geochronological results.  Therefore, we need this entity, too, and can assign a count of 1 to each analysed item.

# Join 1

Uses the [[element_name]] to tie the counted item to the type of plant or body part mentioned (if any) in the `element_name` column of the original dataset.

# Join 2

uses the [[species_split]] to tie the count of 1 to each of the species analysed for each published date in the dataset.

# Join 3

uses the [[unique_row_identifer]] column to tie the count to every "entity" that was analysed for this dataset.

![[images/Entity abundances schema 1.png]]

# YAML as of 2026-08-25

```
name: abundances
type: entity
system_id: system_id
keys: []
columns:
  - species
  - lab_id
  - fid
public_id: abundance_id
source: datasheet_v9
foreign_keys:
  - entity: analysis_entities
    local_keys:
      - lab_no
    remote_keys:
      - lab_no
    how: inner
    constraints:
      cardinality: one_to_many
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
      allow_null_keys: false
      allow_unmatched_left: true
extra_columns:
  abundance: '1'
```
