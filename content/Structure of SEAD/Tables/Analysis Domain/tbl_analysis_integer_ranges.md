---
publish: true
permalink: /Structure of SEAD/Tables/Analysis Domain/tbl_analysis_integer_ranges.md
created: 2026-07-24T09:34:40.874Z
modified: 2026-11-12T06:10:27.857Z
published: 2026-11-12T06:10:27.857Z
table_name: tbl_analysis_integer_ranges
primary_key: "[[analysis_integer_range_id]]"
columns:
  - "[[high_is_uncertain]]"
  - "[[high_value]]"
  - "[[is_variant]]"
  - "[[low_is_uncertain]]"
  - "[[low_value]]"
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

> [!info] Qualified integer range attached to an analysis value.
> Storage for analysis values that represents an integer range.
