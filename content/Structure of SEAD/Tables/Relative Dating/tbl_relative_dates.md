---
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
---

Records the relative dating information for samples by associating a relative age definition with a physical sample through an analysis entity. It includes details about dating methods, notes, and indications of uncertainty (e.g., 'from', 'ca', '<').
