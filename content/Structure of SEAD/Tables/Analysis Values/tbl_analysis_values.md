---
publish: true
permalink: /Structure of SEAD/Tables/Analysis Values/tbl_analysis_values.md
created: 2026-07-24T09:34:40.900Z
modified: 2026-09-23T05:19:09.572Z
published: 2026-09-23T05:19:09.572Z
table_name: tbl_analysis_values
primary_key: "[[analysis_value_id]]"
foreign_keys:
  - "[[analysis_entity_id]]"
  - "[[value_class_id]]"
columns:
  - "[[analysis_value]]"
  - "[[boolean_value]]"
  - "[[is_anomaly]]"
  - "[[is_boolean]]"
  - "[[is_indeterminable]]"
  - "[[is_not_analyzed]]"
  - "[[is_uncertain]]"
  - "[[is_undefined]]"
connected_tables:
  - "[[tbl_analysis_entities]]"
  - "[[tbl_value_classes]]"
change_it: true
---

Stores results from an analysis as a (untyped) string value.
