---
table_name: tbl_ceramics_measurements
primary_key: "[[ceramics_measurement_id]]"
foreign_keys:
  - "[[method_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_methods]]"
---

Contains measurements from ceramic analysis processes.
