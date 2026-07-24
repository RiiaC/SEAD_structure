---
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
