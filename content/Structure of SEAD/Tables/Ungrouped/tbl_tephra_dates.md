---
publish: true
permalink: /Structure of SEAD/Tables/Ungrouped/tbl_tephra_dates.md
created: 2026-07-24T09:34:41.667Z
modified: 2026-11-13T14:41:43.651Z
published: 2026-11-13T14:41:43.651Z
table_name: tbl_tephra_dates
primary_key: "[[tephra_date_id]]"
columns:
  - "[[date_updated]]"
  - "[[notes]]"
connected_tables:
  - "[[tbl_analysis_entities]]"
  - "[[tbl_dating_uncertainty]]"
  - "[[tbl_tephras]]"
foreign_keys:
  - "[[analysis_entity_id]]"
  - "[[dating_uncertainty_id]]"
  - "[[tephra_id]]"
---

Records tephrachronology-based sample dates, including associated uncertainties and additional notes.
