---
table_name: tbl_analysis_boolean_values
primary_key: "[[analysis_boolean_value_id]]"
foreign_keys:
  - "[[analysis_value_id]]"
columns:
  - "[[qualifier]]"
  - "[[value]]"
connected_tables:
  - "[[tbl_analysis_values]]"
---

Stores analysis values that represent a boolean (true/false) condition.
