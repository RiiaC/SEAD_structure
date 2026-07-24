---
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
---

Gives the relationship between sample location types and their respective sampling contexts.
