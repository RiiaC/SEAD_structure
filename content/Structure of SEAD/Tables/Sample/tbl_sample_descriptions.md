---
publish: true
permalink: /Structure of SEAD/Tables/Sample/tbl_sample_descriptions.md
created: 2026-07-24T09:34:41.349Z
modified: 2026-09-24T05:44:40.962Z
published: 2026-09-24T05:44:40.962Z
table_name: tbl_sample_descriptions
primary_key: "[[sample_description_id]]"
foreign_keys:
  - "[[physical_sample_id]]"
  - "[[sample_description_type_id]]"
columns:
  - "[[date_updated]]"
  - "[[Structure of SEAD/Columns/description|description]]"
connected_tables:
  - "[[tbl_physical_samples]]"
  - "[[tbl_sample_description_types]]"
date created: Friday, September 19th 2025, 3:37:16 pm
---

Contains detailed descriptions of samples categorized by different description types.
