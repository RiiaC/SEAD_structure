---
publish: true
permalink: /Structure of SEAD/Tables/Measured Values/tbl_measured_value_dimensions.md
created: 2026-07-24T09:34:41.064Z
modified: 2026-09-23T05:19:10.505Z
published: 2026-09-23T05:19:10.505Z
table_name: tbl_measured_value_dimensions
primary_key: "[[measured_value_dimension_id]]"
columns:
  - "[[date_updated]]"
  - "[[dimension_value]]"
connected_tables:
  - "[[tbl_dimensions]]"
  - "[[tbl_measured_values]]"
foreign_keys:
  - "[[dimension_id]]"
  - "[[measured_value_id]]"
date created: Friday, September 19th 2025, 3:37:16 pm
change_it: true
---

Stores dimensional measurements of samples, such as weight before and after burning, volume, or other similar metrics.
