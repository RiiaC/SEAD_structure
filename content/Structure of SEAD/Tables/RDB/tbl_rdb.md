---
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
publish: true
---

Contains rarity data for taxa within specific geographical areas (e.g., threatened species in Sweden).
