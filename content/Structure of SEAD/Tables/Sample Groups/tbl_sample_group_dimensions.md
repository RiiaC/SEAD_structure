---
table_name: tbl_sample_group_dimensions
primary_key: "[[sample_group_dimension_id]]"
foreign_keys:
  - "[[dimension_id]]"
  - "[[qualifier_id]]"
  - "[[sample_group_id]]"
columns:
  - "[[date_updated]]"
  - "[[dimension_value]]"
connected_tables:
  - "[[tbl_dimensions]]"
  - "[[tbl_value_qualifiers]]"
  - "[[tbl_sample_groups]]"
---

Contains the physical dimensions of a sample group (e.g., core length) based on a specified dimension type.
