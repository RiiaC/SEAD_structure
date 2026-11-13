---
table_name: tbl_ceramics_lookup
primary_key: "[[ceramics_lookup_id]]"
foreign_keys:
  - "[[method_id]]"
columns:
  - "[[date_updated]]"
  - "[[description]]"
  - "[[name]]"
connected_tables:
  - "[[tbl_methods]]"
publish: true
---

Serves as a reference for ceramic types and their associated details.
