---
publish: true
permalink: /Structure of SEAD/Tables/Sample Groups/tbl_sample_group_descriptions.md
created: 2026-07-24T09:34:41.225Z
modified: 2026-10-02T09:16:37.233Z
published: 2026-10-02T09:16:37.233Z
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
---

Contains definitions or descriptions of groups of samples, categorized by a specific description type.
