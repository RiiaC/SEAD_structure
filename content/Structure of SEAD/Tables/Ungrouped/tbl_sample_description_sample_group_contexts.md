---
publish: true
permalink: /Structure of SEAD/Tables/Ungrouped/tbl_sample_description_sample_group_contexts.md
created: 2026-07-24T09:34:41.635Z
modified: 2026-09-24T05:44:41.423Z
published: 2026-09-24T05:44:41.423Z
table_name: tbl_sample_description_sample_group_contexts
primary_key: "[[sample_description_sample_group_context_id]]"
foreign_keys:
  - "[[sample_description_type_id]]"
  - "[[sampling_context_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_sample_description_types]]"
  - "[[tbl_sample_group_sampling_contexts]]"
---

Links sample descriptions to their respective group contexts, providing a structured way to manage and categorize sample data.
