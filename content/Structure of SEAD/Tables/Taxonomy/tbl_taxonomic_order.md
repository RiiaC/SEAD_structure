---
table_name: tbl_taxonomic_order
primary_key: "[[taxonomic_order_id]]"
foreign_keys:
  - "[[taxon_id]]"
  - "[[taxonomic_order_system_id]]"
columns:
  - "[[date_updated]]"
  - "[[taxonomic_code]]"
connected_tables:
  - "[[tbl_taxa_tree_master]]"
  - "[[tbl_taxonomic_order_systems]]"
---

Contains taxonomic codes for organizing species within a taxonomic hierarchy or referencing external database systems (e.g., GBIF, Artdatabanken).
