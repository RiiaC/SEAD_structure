---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity analysis_value.md
created: 2026-09-15T10:31:11.671Z
modified: 2026-09-23T05:19:01.134Z
published: 2026-09-23T05:19:01.134Z
Entity_Name: analysis_value
Type: Data (Derived)
Source_entity: "[[Example dataset mapping/Strucke Data-mapping/Entity datasheet|Entity datasheet]]"
Public_ID: analysis_value_id
columns:
  - "[[pMC_error]]"
  - "[[pMC_value]]"
  - "[[unique_row_identifer]]"
Target_Entity: "[[Entity analysis_entity]]"
Local_Keys:
  - "[[unique_row_identifer]]"
Remote_Keys:
  - "[[unique_row_identifer]]"
SEAD_table: "[[tbl_analysis_values]]"
status: complete
Target_Entity_2: "[[Entity value_class]]"
Local_Keys_2: "[[value_type_name]]"
Remote_Keys_2: "[[name]]"
change_it: true
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
