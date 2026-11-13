---
publish: true
permalink: /Structure of SEAD/Tables/Core Domain/Project/tbl_projects.md
created: 2026-07-24T09:34:41.162Z
modified: 2026-11-13T16:42:47.550Z
published: 2026-11-13T16:42:47.550Z
table_name: tbl_projects
primary_key: "[[project_id]]"
columns:
  - "[[date_updated]]"
  - "[[description]]"
  - "[[project_abbrev_name]]"
  - "[[project_name]]"
connected_tables:
  - "[[tbl_project_stages]]"
  - "[[tbl_project_types]]"
foreign_keys:
  - "[[project_stage_id]]"
  - "[[project_type_id]]"
required: No
role: lookup
domain:
  - core
  - provenance
---

> [!abstract] Project-level metadata referenced by datasets and site collections.
> Contains information about projects, including their names and descriptions, pertinent to datasets for specific sites.
