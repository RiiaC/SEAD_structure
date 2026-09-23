---
publish: true
permalink: /Structure of SEAD/Tables/Sample Groups/tbl_sample_group_descriptions.md
created: 2026-07-24T09:34:41.225Z
modified: 2026-09-23T05:19:10.821Z
published: 2026-09-23T05:19:10.821Z
table_name: tbl_sample_group_descriptions
primary_key: "[[sample_group_description_id]]"
foreign_keys:
  - "[[sample_group_description_type_id]]"
  - "[[sample_group_id]]"
columns:
  - "[[date_updated]]"
  - "[[group_description]]"
connected_tables:
  - "[[tbl_sample_group_description_types]]"
  - "[[tbl_sample_groups]]"
date created: Friday, September 19th 2025, 3:37:16 pm
change_it: true
---

Contains definitions or descriptions of groups of samples, categorized by a specific description type.
