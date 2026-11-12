---
publish: true
permalink: /Structure of SEAD/Tables/Analysis Domain/tbl_analysis_numerical_ranges.md
created: 2026-07-24T09:34:40.887Z
modified: 2026-11-12T06:12:04.277Z
published: 2026-11-12T06:12:04.277Z
table_name: tbl_analysis_numerical_ranges
primary_key: "[[analysis_numerical_range_id]]"
columns:
  - "[[high_is_uncertain]]"
  - "[[is_variant]]"
  - "[[low_is_uncertain]]"
  - "[[value]]"
connected_tables:
  - "[[tbl_analysis_values]]"
  - "[[tbl_value_qualifier_symbols]]"
foreign_keys:
  - "[[analysis_value_id]]"
  - "[[high_qualifier]]"
  - "[[low_qualifier]]"
required: No
role: fact
domain:
  - analysis
---

> [!info] Numerical range stored in the SEAD `numrange` column format and attached to an analysis value.
> Storage for analysis values that represents a numerical range.
