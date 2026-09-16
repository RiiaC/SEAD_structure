---
publish: true
permalink: /Example dataset mapping/Strucke datamapping with Brunos code/Entity abundance.md
modified: 2026-09-16T14:00:43.917Z
---

> [!info] we don't have counts of the things that were dated, but we do know that at least one something had to be present to have been dated,
> and in SEAD it is the abundances table that become an analysis entity, which in turn has analysis values and/or geochronological results.  Therefore, we need this entity, too.
> It is joined to three other

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
