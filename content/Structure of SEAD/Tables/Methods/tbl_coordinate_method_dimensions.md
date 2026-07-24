---
table_name: tbl_coordinate_method_dimensions
primary_key: "[[coordinate_method_dimension_id]]"
foreign_keys:
  - "[[dimension_id]]"
  - "[[method_id]]"
columns:
  - "[[date_updated]]"
  - "[[limit_lower]]"
  - "[[limit_upper]]"
connected_tables:
  - "[[tbl_dimensions]]"
  - "[[tbl_methods]]"
date created: Friday, September 19th 2025, 3:37:16 pm
---

Defines the dimensions applicable to each coordinate system method and specifies any legal values for these dimensions. Each entry associates a coordinate system method with its corresponding dimensions and their permissible value ranges.
