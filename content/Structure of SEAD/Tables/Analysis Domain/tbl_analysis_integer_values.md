---
publish: true
permalink: /Structure of SEAD/Tables/Analysis Domain/tbl_analysis_integer_values.md
created: 2026-07-24T09:34:40.876Z
modified: 2026-11-13T16:38:00.842Z
published: 2026-11-13T16:38:00.842Z
table_name: tbl_analysis_integer_values
primary_key: "[[analysis_integer_value_id]]"
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

> [!abstract] Integer-valued analysis result with an optional qualifier symbol.
> Storage for analysis values that represents an integer value.
