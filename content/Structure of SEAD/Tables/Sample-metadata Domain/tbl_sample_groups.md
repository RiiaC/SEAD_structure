---
publish: true
permalink: /Structure of SEAD/Tables/Sample-metadata Domain/tbl_sample_groups.md
created: 2026-07-24T09:34:41.216Z
modified: 2026-11-16T08:33:24.510Z
published: 2026-11-16T08:33:24.510Z
table_name: tbl_sample_groups
primary_key: "[[sample_group_id]]"
columns:
  - "[[date_updated]]"
  - "[[sample_group_description]]"
  - "[[sample_group_name]]"
  - "[[sample_group_uuid]]"
connected_tables:
  - "[[tbl_methods]]"
  - "[[tbl_sample_group_sampling_contexts]]"
  - "[[tbl_sites]]"
foreign_keys:
  - "[[method_id]]"
  - "[[sampling_context_id]]"
  - "[[site_id]]"
  - "[[tbl_locations]]"
---

Contains collections of related samples, typically grouped by structures (e.g., House 1), stratigraphic sequences (e.g., profile 3), or lake cores. Groups can be defined flexibly based on research needs.
