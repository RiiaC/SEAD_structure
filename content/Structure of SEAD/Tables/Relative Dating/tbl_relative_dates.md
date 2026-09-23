---
publish: true
permalink: /Structure of SEAD/Tables/Relative Dating/tbl_relative_dates.md
created: 2026-07-24T09:34:41.201Z
modified: 2026-09-23T05:19:10.739Z
published: 2026-09-23T05:19:10.739Z
table_name: tbl_relative_dates
primary_key: "[[relative_date_id]]"
foreign_keys:
  - "[[analysis_entity_id]]"
  - "[[dating_uncertainty_id]]"
  - "[[method_id]]"
  - "[[relative_age_id]]"
columns:
  - "[[date_updated]]"
  - "[[notes]]"
connected_tables:
  - "[[tbl_analysis_entities]]"
  - "[[tbl_dating_uncertainty]]"
  - "[[tbl_methods]]"
  - "[[tbl_relative_ages]]"
change_it: true
---

Records the relative dating information for samples by associating a relative age definition with a physical sample through an analysis entity. It includes details about dating methods, notes, and indications of uncertainty (e.g., 'from', 'ca', '<').
