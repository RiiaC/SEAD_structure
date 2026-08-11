---
table_name: tbl_sample_groups
primary_key: "[[sample_group_id]]"
foreign_keys:
  - "[[method_id]]"
  - "[[sampling_context_id]]"
  - "[[site_id]]"
  - "[[tbl_locations]]"
columns:
  - "[[date_updated]]"
  - "[[sample_group_description]]"
  - "[[sample_group_name]]"
  - "[[sample_group_uuid]]"
connected_tables:
  - "[[tbl_methods]]"
  - "[[tbl_sample_group_sampling_contexts]]"
  - "[[tbl_sites]]"
date created: Friday, September 19th 2025, 3:37:16 pm
publish: true
---
Contains collections of related samples, typically grouped by structures (e.g., House 1), stratigraphic sequences (e.g., profile 3), or lake cores. Groups can be defined flexibly based on research needs.
