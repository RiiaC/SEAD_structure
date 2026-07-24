---
table_name: tbl_sample_colours
primary_key: "[[sample_colour_id]]"
foreign_keys:
  - "[[colour_id]]"
  - "[[physical_sample_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_colours]]"
  - "[[tbl_physical_samples]]"
---

Contains information about the colors related to physical samples.
