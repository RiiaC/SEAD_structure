---
table_name: tbl_analysis_integer_ranges
primary_key: "[[analysis_integer_range_id]]"
foreign_keys:
  - "[[analysis_value_id]]"
  - "[[high_qualifier]]"
  - "[[low_qualifier]]"
columns:
  - "[[high_is_uncertain]]"
  - "[[high_value]]"
  - "[[is_variant]]"
  - "[[low_is_uncertain]]"
  - "[[low_value]]"
connected_tables:
  - "[[tbl_analysis_values]]"
  - "[[tbl_value_qualifier_symbols]]"
---

Storage for analysis values that represents an integer range.
