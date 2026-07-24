---
table_name: tbl_sample_group_description_type_sampling_contexts
primary_key: "[[sample_group_description_type_sampling_context_id]]"
foreign_keys:
  - "[[sample_group_description_type_id]]"
  - "[[sampling_context_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_sample_group_description_types]]"
  - "[[tbl_sample_group_sampling_contexts]]"
---

Associates description types with sampling methods. Specifically used for dendrochronology to group description types based on detail levels, indicating how fields relate to dendrochronological analysis of buildings.
