---
table_name: tbl_rdb_systems
primary_key: "[[rdb_system_id]]"
foreign_keys:
  - "[[biblio_id]]"
  - "[[location_id]]"
columns:
  - "[[date_updated]]"
  - "[[rdb_first_published]]"
  - "[[rdb_system]]"
  - "[[rdb_system_date]]"
  - "[[rdb_system_uuid]]"
  - "[[rdb_version]]"
connected_tables:
  - "[[tbl_biblio]]"
  - "[[tbl_locations]]"
---

Details of rarity designation systems (commonly known as Red Data Books) and the regions where they are applicable.
