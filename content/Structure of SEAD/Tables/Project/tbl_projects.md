---
publish: true
permalink: /Structure of SEAD/Tables/Project/tbl_projects.md
created: 2026-07-24T09:34:41.162Z
modified: 2026-10-02T09:16:37.102Z
published: 2026-10-02T09:16:37.102Z
table_name: tbl_projects
primary_key: "[[project_id]]"
foreign_keys:
  - "[[project_stage_id]]"
  - "[[project_type_id]]"
columns:
  - "[[date_updated]]"
  - "[[description]]"
  - "[[project_abbrev_name]]"
  - "[[project_name]]"
connected_tables:
  - "[[tbl_project_stages]]"
  - "[[tbl_project_types]]"
---

Contains information about projects, including their names and descriptions, pertinent to datasets for specific sites.
