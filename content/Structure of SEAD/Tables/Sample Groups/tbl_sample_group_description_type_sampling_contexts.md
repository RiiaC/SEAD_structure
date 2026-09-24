---
publish: true
permalink: /Structure of SEAD/Tables/Sample Groups/tbl_sample_group_description_type_sampling_contexts.md
created: 2026-07-24T09:34:41.239Z
modified: 2026-09-24T05:44:41.034Z
published: 2026-09-24T05:44:41.034Z
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
