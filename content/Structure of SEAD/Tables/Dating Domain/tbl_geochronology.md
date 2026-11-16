---
publish: true
permalink: /Structure of SEAD/Tables/Dating Domain/tbl_geochronology.md
created: 2026-07-24T09:34:41.028Z
modified: 2026-11-16T13:38:08.431Z
published: 2026-11-16T13:38:08.431Z
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
  - "[[Structure of SEAD/Columns/lab_number]]"
foreign_keys:
  - "[[analysis_entity_id]]"
  - "[[dating_lab_id]]"
  - "[[dating_uncertainty_id]]"
connected_tables:
  - "[[tbl_analysis_entities]]"
  - "[[tbl_dating_labs]]"
  - "[[tbl_dating_uncertainty]]"
required: No
role: fact
domain:
  - dating
---

> [!abstract] Absolute or chronology dating observation linked to an analysis entity and optionally to a dating laboratory; Arbodat chronology/lab dating facts map here even when the project-local entity is named `dating`.
> Contains radiometric dating information for samples, primarily radiocarbon, but also includes other methods such as Uranium series. These are also referred to as absolute dates.
