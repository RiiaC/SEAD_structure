---
publish: true
permalink: /Structure of SEAD/Tables/Geochronology/tbl_geochronology.md
created: 2026-07-24T09:34:41.028Z
modified: 2026-09-23T05:19:10.090Z
published: 2026-09-23T05:19:10.090Z
table_name: tbl_geochronology
primary_key: "[[geochron_id]]"
foreign_keys:
  - "[[analysis_entity_id]]"
  - "[[dating_lab_id]]"
  - "[[dating_uncertainty_id]]"
columns:
  - "[[age]]"
  - "[[date_updated]]"
  - "[[delta_13c]]"
  - "[[error_older]]"
  - "[[error_younger]]"
  - "[[geochron_uuid]]"
  - "[[Structure of SEAD/Columns/lab_number]]"
  - "[[notes]]"
connected_tables:
  - "[[tbl_analysis_entities]]"
  - "[[tbl_dating_labs]]"
  - "[[tbl_dating_uncertainty]]"
date created: Friday, September 19th 2025, 3:37:16 pm
change_it: true
---

Contains radiometric dating information for samples, primarily radiocarbon, but also includes other methods such as Uranium series. These are also referred to as absolute dates.
