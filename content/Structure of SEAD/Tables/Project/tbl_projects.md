---
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
date created: Friday, September 19th 2025, 3:37:16 pm
publish: true
---

Contains information about projects, including their names and descriptions, pertinent to datasets for specific sites.
