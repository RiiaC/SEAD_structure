---
table_name: tbl_analysis_integer_values
primary_key: "[[analysis_integer_value_id]]"
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

Storage for analysis values that represents an integer value.
