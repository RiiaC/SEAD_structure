---
table_name: tbl_lithology
primary_key: "[[lithology_id]]"
foreign_keys:
  - "[[sample_group_id]]"
columns:
  - "[[date_updated]]"
  - "[[depth_bottom]]"
  - "[[depth_top]]"
  - "[[source/docs/plugins/Description]]"
  - "[[lower_boundary]]"
connected_tables:
  - "[[tbl_sample_groups]]"
---

Provides a detailed description of sedimentary units within a sample group. It allows for the characterization of a soil profile at various depths, corresponding to the sample depths (e.g., 0-10 cm: humus, 10-30 cm: sand).
