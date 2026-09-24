---
publish: true
permalink: /Structure of SEAD/Tables/Dendro/tbl_dendro_dates.md
created: 2026-07-24T09:34:40.974Z
modified: 2026-09-24T05:44:40.585Z
published: 2026-09-24T05:44:40.585Z
table_name: tbl_dendro_dates
primary_key: "[[dendro_date_id]]"
foreign_keys:
  - "[[age_type_id]]"
  - "[[analysis_entity_id]]"
  - "[[dating_uncertainty_id]]"
  - "[[dendro_lookup_id]]"
columns:
  - "[[age_older]]"
  - "[[age_range]]"
  - "[[age_younger]]"
  - "[[date_updated]]"
  - "[[season_id]]"
connected_tables:
  - "[[tbl_age_types]]"
  - "[[tbl_analysis_entities]]"
  - "[[tbl_dating_uncertainty]]"
  - "[[tbl_dendro_lookup]]"
date created: Friday, September 19th 2025, 3:37:16 pm
---

20130722PIB: Added field dating\_uncertainty\_id to cater for >< etc. 20130722pib: prefixed fieldnames age\_younger and age\_older with "cal\_" to conform with equivalent names in other tables
