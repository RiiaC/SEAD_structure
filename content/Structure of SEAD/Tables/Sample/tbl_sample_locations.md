---
publish: true
permalink: /Structure of SEAD/Tables/Sample/tbl_sample_locations.md
created: 2026-07-24T09:34:41.370Z
modified: 2026-09-24T05:44:40.996Z
published: 2026-09-24T05:44:40.996Z
table_name: tbl_sample_locations
primary_key: "[[sample_location_id]]"
foreign_keys:
  - "[[physical_sample_id]]"
  - "[[sample_location_type_id]]"
columns:
  - "[[date_updated]]"
  - "[[location]]"
connected_tables:
  - "[[tbl_physical_samples]]"
  - "[[tbl_sample_location_types]]"
date created: Friday, September 19th 2025, 3:37:16 pm
---

Contains information about the locations of samples based on predefined types.
