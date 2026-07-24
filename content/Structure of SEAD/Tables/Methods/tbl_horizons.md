---
table_name: tbl_horizons
primary_key: "[[horizon_id]]"
foreign_keys:
  - "[[method_id]]"
columns:
  - "[[date_updated]]"
  - "[[source/docs/plugins/Description]]"
  - "[[horizon_name]]"
connected_tables:
  - "[[tbl_methods]]"
---

Represents the layer of soil from which samples are taken, classified according to a recognized standard (e.g., FAO A horizon).
