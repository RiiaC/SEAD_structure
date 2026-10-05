---
publish: true
permalink: /Structure of SEAD/Tables/Measured Values/tbl_measured_values.md
created: 2026-07-24T09:34:41.064Z
modified: 2026-10-02T09:16:37.048Z
published: 2026-10-02T09:16:37.048Z
table_name: tbl_measured_values
primary_key: "[[measured_value_id]]"
foreign_keys:
  - "[[analysis_entity_id]]"
columns:
  - "[[date_updated]]"
  - "[[measured_value]]"
connected_tables:
  - "[[tbl_analysis_entities]]"
---

Records continuous chemical or physical values related to specific sample analyses. Each Sample Analysis can have zero or one associated Measured Value.
