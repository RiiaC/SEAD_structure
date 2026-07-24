---
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
