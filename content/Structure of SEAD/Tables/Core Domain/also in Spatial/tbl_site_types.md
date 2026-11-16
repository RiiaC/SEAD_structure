---
publish: true
permalink: /Structure of SEAD/Tables/Core Domain/also in Spatial/tbl_site_types.md
created: 2026-11-16T10:15:41.570Z
modified: 2026-11-16T10:18:16.561Z
published: 2026-11-16T10:18:16.561Z
table_name: tbl_site_types
primary_key: "[[site_type_id]]"
columns:
  - "[[description]]"
  - "[[site_type_abbrev]]"
  - "[[site_type]]"
connected_tables:
  - "[[tbl_site_type_groups]]"
foreign_keys:
  - "[[site_type_group_id]]"
role: classifier
required: No
domain:
  - core
  - spatial
---

> [!abstract] Controlled vocabulary for site classification in SEAD.
