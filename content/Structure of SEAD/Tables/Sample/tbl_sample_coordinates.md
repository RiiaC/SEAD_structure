---
publish: true
permalink: /Structure of SEAD/Tables/Sample/tbl_sample_coordinates.md
created: 2026-07-24T09:34:41.343Z
modified: 2026-10-02T09:16:37.143Z
published: 2026-10-02T09:16:37.143Z
table_name: tbl_sample_coordinates
primary_key: "[[sample_coordinate_id]]"
foreign_keys:
  - "[[coordinate_method_dimension_id]]"
  - "[[physical_sample_id]]"
  - "[[coordinate_method_dimension_id]]"
columns:
  - "[[accuracy]]"
  - "[[date_updated]]"
  - "[[measurement]]"
connected_tables:
  - "[[tbl_coordinate_method_dimensions]]"
  - "[[tbl_physical_samples]]"
---

Specifies the physical location data of samples. This includes both local grid references and standardized global coordinates, such as latitude and longitude. References a methods that determines the type of grid used, facilitating the plotting of samples on large-scale maps or site-specific projects.
