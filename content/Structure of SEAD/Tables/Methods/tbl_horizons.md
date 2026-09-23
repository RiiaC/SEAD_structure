---
publish: true
permalink: /Structure of SEAD/Tables/Methods/tbl_horizons.md
created: 2026-07-24T09:34:41.136Z
modified: 2026-09-23T05:19:10.379Z
published: 2026-09-23T05:19:10.379Z
table_name: tbl_horizons
primary_key: "[[horizon_id]]"
foreign_keys:
  - "[[method_id]]"
columns:
  - "[[date_updated]]"
  - "[[description]]"
  - "[[horizon_name]]"
connected_tables:
  - "[[tbl_methods]]"
change_it: true
---

Represents the layer of soil from which samples are taken, classified according to a recognized standard (e.g., FAO A horizon).
