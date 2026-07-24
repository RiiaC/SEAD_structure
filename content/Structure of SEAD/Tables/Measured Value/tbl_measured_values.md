---
table_name: tbl_measured_values
primary_key: "[[measured_value_id]]"
foreign_keys:
  - "[[analysis_entity_id]]"
columns:
  - "[[date_updated]]"
  - "[[measured_value]]"
connected_tables:
  - "[[tbl_analysis_entities]]"
date created: Friday, September 19th 2025, 3:37:16 pm
---

Records continuous chemical or physical values related to specific sample analyses. Each Sample Analysis can have zero or one associated Measured Value.
