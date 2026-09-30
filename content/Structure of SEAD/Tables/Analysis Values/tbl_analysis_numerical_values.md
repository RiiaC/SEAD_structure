---
publish: true
permalink: /Structure of SEAD/Tables/Analysis Values/tbl_analysis_numerical_values.md
created: 2026-07-24T09:34:40.892Z
modified: 2026-09-30T10:44:42.282Z
published: 2026-09-30T10:44:42.282Z
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
---

Storage for analysis values that represents a numerical.
