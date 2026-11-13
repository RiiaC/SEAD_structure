---
publish: true
permalink: /Structure of SEAD/Tables/Analysis Domain/tbl_analysis_numerical_values.md
created: 2026-07-24T09:34:40.892Z
modified: 2026-11-13T16:36:45.691Z
published: 2026-11-13T16:36:45.691Z
table_name: tbl_analysis_numerical_values
primary_key: "[[analysis_numerical_value_id]]"
columns:
  - "[[is_variant]]"
  - "[[value]]"
connected_tables:
  - "[[tbl_analysis_values]]"
  - "[[tbl_value_qualifier_symbols]]"
foreign_keys:
  - "[[analysis_value_id]]"
  - "[[qualifier]]"
required: No
role: fact
domain:
  - analysis
---

> [!abstract] Numerical analysis result with an optional qualifier symbol.
> Storage for analysis values that represents a numerical.
