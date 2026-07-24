---
table_name: tbl_ecocode_systems
primary_key: "[[ecocode_system_id]]"
foreign_keys:
  - "[[biblio_id]]"
columns:
  - "[[date_updated]]"
  - "[[definition]]"
  - "[[ecocode_system_uuid]]"
  - "[[name]]"
  - "[[notes]]"
connected_tables:
  - "[[tbl_biblio]]"
---

Defines various systems used for classifying specific attributes of taxa, including habitat preferences, food types, and cultural uses.
