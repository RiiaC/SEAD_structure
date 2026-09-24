---
publish: true
permalink: /Structure of SEAD/Tables/Sample Groups/tbl_sample_group_coordinates.md
created: 2026-07-24T09:34:41.218Z
modified: 2026-09-24T05:44:41.012Z
published: 2026-09-24T05:44:41.012Z
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
