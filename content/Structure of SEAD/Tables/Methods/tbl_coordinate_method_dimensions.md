---
publish: true
permalink: /Structure of SEAD/Tables/Methods/tbl_coordinate_method_dimensions.md
created: 2026-07-24T09:34:41.127Z
modified: 2026-09-24T05:44:40.823Z
published: 2026-09-24T05:44:40.823Z
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
