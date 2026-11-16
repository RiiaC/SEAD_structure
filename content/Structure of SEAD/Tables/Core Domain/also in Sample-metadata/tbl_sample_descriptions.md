---
publish: true
permalink: /Structure of SEAD/Tables/Core Domain/also in Sample-metadata/tbl_sample_descriptions.md
created: 2026-07-24T09:34:41.349Z
modified: 2026-11-16T08:09:14.163Z
published: 2026-11-16T08:09:14.163Z
table_name: tbl_sample_descriptions
primary_key: "[[sample_description_id]]"
columns:
  - "[[date_updated]]"
  - "[[description|description]]"
connected_tables:
  - "[[tbl_physical_samples]]"
  - "[[tbl_sample_description_types]]"
foreign_keys:
  - "[[physical_sample_id]]"
  - "[[sample_description_type_id]]"
role: fact
required: No
domain:
  - core
  - sample-metadata
---

> [!abstract] Typed free-text or coded description attached to a physical sample.
> Contains detailed descriptions of samples categorized by different description types.
