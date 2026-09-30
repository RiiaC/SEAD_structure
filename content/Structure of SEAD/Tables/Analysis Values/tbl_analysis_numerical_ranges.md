---
publish: true
permalink: /Structure of SEAD/Tables/Analysis Values/tbl_analysis_numerical_ranges.md
created: 2026-07-24T09:34:40.887Z
modified: 2026-09-30T10:44:40.771Z
published: 2026-09-30T10:44:40.771Z
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
---

Storage for analysis values that represents a numerical range.
