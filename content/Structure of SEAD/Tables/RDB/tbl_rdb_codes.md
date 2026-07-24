---
table_name: tbl_rdb_codes
primary_key: "[[rdb_code_id]]"
foreign_keys:
  - "[[rdb_system_id]]"
columns:
  - "[[date_updated]]"
  - "[[rdb_category]]"
  - "[[rdb_definition]]"
connected_tables:
  - "[[tbl_rdb_systems]]"
---

Definitions of rarity categories across various systems, as specified in tbl_rdb_systems.
