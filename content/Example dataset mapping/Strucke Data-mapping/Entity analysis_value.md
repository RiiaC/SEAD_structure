---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity analysis_value.md
modified: 2026-09-17T16:06:22.452Z
---

> [!info] this table uses the joins to connect the analysis values reported for percent modern carbon (pMC) and its error to the labels showing which values are the pMC, and which the error

# YAML as of 2026-09-17

```
name: analysis_value
type: entity
system_id: system_id
keys: []
columns:
  - unique_row_identifier
  - pmc_value
  - pmc_error
public_id: analysis_value_id
source: datasheet
foreign_keys:
  - entity: analysis_entity
    local_keys:
      - unique_row_identifier
    remote_keys:
      - unique_row_identifier
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
      allow_unmatched_left: true
  - entity: value_class
    local_keys:
      - value_type_name
    remote_keys:
      - name
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
drop_empty_rows:
  - analysis_value
unnest:
  id_vars:
    - unique_row_identifier
  value_vars:
    - pmc_value
    - pmc_error
  var_name: value_type_name
  value_name: analysis_value
```

```
```
