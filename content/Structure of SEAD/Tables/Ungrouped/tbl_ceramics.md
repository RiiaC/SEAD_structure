---
table_name: tbl_ceramics
primary_key: "[[ceramics_id]]"
foreign_keys:
  - "[[analysis_entity_id]]"
  - "[[ceramics_lookup_id]]"
columns:
  - "[[date_updated]]"
  - "[[measurement_value]]"
connected_tables:
  - "[[tbl_analysis_entities]]"
  - "[[tbl_ceramics_lookup]]"
---

Stores analysis results from ceramic thin-sections and sherds.
