---
table_name: tbl_sample_horizons
primary_key: "[[sample_horizon_id]]"
foreign_keys:
  - "[[horizon_id]]"
  - "[[physical_sample_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_horizons]]"
  - "[[tbl_physical_samples]]"
---

Represents the specific soil layer from which a sample is collected.
