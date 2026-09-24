---
publish: true
permalink: /Structure of SEAD/Tables/Analysis Values/tbl_analysis_numerical_values.md
created: 2026-07-24T09:34:40.892Z
modified: 2026-09-24T05:44:40.502Z
published: 2026-09-24T05:44:40.502Z
table_name: tbl_analysis_numerical_values
primary_key: "[[analysis_numerical_value_id]]"
foreign_keys:
  - "[[analysis_value_id]]"
  - "[[qualifier]]"
columns:
  - "[[is_variant]]"
  - "[[value]]"
connected_tables:
  - "[[tbl_analysis_values]]"
  - "[[tbl_value_qualifier_symbols]]"
---

Storage for analysis values that represents a numerical.
