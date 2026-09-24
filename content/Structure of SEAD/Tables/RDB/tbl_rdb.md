---
publish: true
permalink: /Structure of SEAD/Tables/RDB/tbl_rdb.md
created: 2026-07-24T09:34:41.181Z
modified: 2026-09-24T05:44:40.884Z
published: 2026-09-24T05:44:40.884Z
table_name: tbl_rdb
primary_key: "[[rdb_id]]"
foreign_keys:
  - "[[location_id]]"
  - "[[rdb_code_id]]"
  - "[[taxon_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_rdb_codes]]"
  - "[[tbl_taxa_tree_master]]"
  - "[[tbl_locations]]"
---

Contains rarity data for taxa within specific geographical areas (e.g., threatened species in Sweden).
