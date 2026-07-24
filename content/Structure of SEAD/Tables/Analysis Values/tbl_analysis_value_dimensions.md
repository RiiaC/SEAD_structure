---
table_name: tbl_analysis_value_dimensions
primary_key: "[[analysis_value_dimension_id]]"
foreign_keys:
  - "[[analysis_value_id]]"
  - "[[dimension_id]]"
columns:
  - "[[value]]"
connected_tables:
  - "[[tbl_analysis_values]]"
  - "[[tbl_dimensions]]"
---

Storage for dimension of analysis value.
