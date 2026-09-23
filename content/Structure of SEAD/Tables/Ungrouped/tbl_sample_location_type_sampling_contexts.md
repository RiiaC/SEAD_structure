---
publish: true
permalink: /Structure of SEAD/Tables/Ungrouped/tbl_sample_location_type_sampling_contexts.md
created: 2026-07-24T09:34:41.642Z
modified: 2026-09-23T05:19:12.556Z
published: 2026-09-23T05:19:12.556Z
table_name: tbl_sample_location_type_sampling_contexts
primary_key: "[[sample_location_type_sampling_context_id]]"
foreign_keys:
  - "[[sample_location_type_id]]"
  - "[[sampling_context_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_sample_location_types]]"
  - "[[tbl_sample_group_sampling_contexts]]"
change_it: true
---

Gives the relationship between sample location types and their respective sampling contexts.
