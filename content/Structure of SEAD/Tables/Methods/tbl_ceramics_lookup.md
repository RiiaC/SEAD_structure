---
table_name: tbl_ceramics_lookup
primary_key: "[[ceramics_lookup_id]]"
foreign_keys:
  - "[[method_id]]"
columns:
  - "[[date_updated]]"
  - "[[source/docs/plugins/Description]]"
  - "[[name]]"
connected_tables:
  - "[[tbl_methods]]"
---

Serves as a reference for ceramic types and their associated details.
