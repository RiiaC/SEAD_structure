---
publish: true
permalink: /Example dataset mapping/AFL Radiocarbon Data mapping/Entity abundance_modifications.md
---

> [!info] the table Tom suggested, on 2026-02-19, to use for the [[C. Biological Age]], as it is a characteristic of the bone being sampled

- create a data-derived entity for abundance\_modifications, and add the column biological\_age
- join it to the [[Entity modification_types]] where biological age = modification\_type\_name _(this attempted 2026-04-22, but ran into errors--Roger is looking into them)_

![[images/Entity abundance_modifications schema.png]]

# YAML

```
name: abundance_modifications
type: entity
system_id: system_id
keys: []
columns:
  - lab_nr
  - biological_age
public_id: abundance_modification_id
source: datasheet
foreign_keys:
  - entity: modification_types
    local_keys:
      - biological_age
    remote_keys:
      - modification_type_name
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
      allow_null_keys: false
drop_empty_rows:
  - biological_age
```
