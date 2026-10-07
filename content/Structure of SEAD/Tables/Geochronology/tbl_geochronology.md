---
publish: true
permalink: /Structure of SEAD/Tables/Geochronology/tbl_geochronology.md
created: 2026-07-24T09:34:41.028Z
modified: 2026-10-06T14:43:30.096Z
published: 2026-10-06T14:43:30.096Z
table_name: tbl_geochronology
primary_key: "[[geochron_id]]"
columns:
  - "[[age]]"
  - "[[date_updated]]"
  - "[[delta_13c]]"
  - "[[error_older]]"
  - "[[error_younger]]"
  - "[[geochron_uuid]]"
  - "[[notes]]"
  - "[[Structure of SEAD/Tables/Columns/lab_number]]"
connected_tables:
  - "[[tbl_analysis_entities]]"
  - "[[tbl_dating_labs]]"
  - "[[tbl_dating_uncertainty]]"
foreign_keys:
  - "[[analysis_entity_id]]"
  - "[[dating_lab_id]]"
  - "[[dating_uncertainty_id]]"
---

Contains radiometric dating information for samples, primarily radiocarbon, but also includes other methods such as Uranium series. These are also referred to as absolute dates.
