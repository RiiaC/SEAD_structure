---
table_name: tbl_analysis_categorical_values
primary_key: "[[analysis_categorical_value_id]]"
foreign_keys:
  - "[[analysis_value_id]]"
  - "[[value_type_item_id]]"
columns:
  - "[[is_variant]]"
  - "[[value]]"
connected_tables:
  - "[[tbl_analysis_values]]"
  - "[[tbl_value_type_items]]"
---

Storage for analysis values that represents a categorical value.
