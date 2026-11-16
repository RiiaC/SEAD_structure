---
publish: true
permalink: /Structure of SEAD/Tables/Ungrouped/tbl_lithology.md
created: 2026-07-24T09:34:41.210Z
modified: 2026-11-16T08:32:32.566Z
published: 2026-11-16T08:32:32.566Z
table_name: tbl_lithology
primary_key: "[[lithology_id]]"
columns:
  - "[[date_updated]]"
  - "[[depth_bottom]]"
  - "[[depth_top]]"
  - "[[description]]"
  - "[[lower_boundary]]"
connected_tables:
  - "[[tbl_sample_groups]]"
foreign_keys:
  - "[[sample_group_id]]"
---

Provides a detailed description of sedimentary units within a sample group. It allows for the characterization of a soil profile at various depths, corresponding to the sample depths (e.g., 0-10 cm: humus, 10-30 cm: sand).
