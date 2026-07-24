---
table_name: tbl_tephra_dates
primary_key: "[[tephra_date_id]]"
foreign_keys:
  - "[[analysis_entity_id]]"
  - "[[dating_uncertainty_id]]"
  - "[[tephra_id]]"
columns:
  - "[[date_updated]]"
  - "[[notes]]"
connected_tables:
  - "[[tbl_analysis_entities]]"
  - "[[tbl_dating_uncertainty]]"
  - "[[tbl_tephras]]"
---

Records tephrachronology-based sample dates, including associated uncertainties and additional notes.
