---
table_name: tbl_sample_group_coordinates
primary_key: "[[sample_group_position_id]]"
foreign_keys:
  - "[[coordinate_method_dimension_id]]"
  - "[[sample_group_id]]"
columns:
  - "[[date_updated]]"
  - "[[position_accuracy]]"
  - "[[sample_group_position]]"
connected_tables:
  - "[[tbl_coordinate_method_dimensions]]"
  - "[[tbl_sample_groups]]"
date created: Friday, September 19th 2025, 3:37:16 pm
---

Contains coordinates related to sample groups, such as the top of a core, the top of a profile, or specific locations on dendrochronological or ceramic objects.
