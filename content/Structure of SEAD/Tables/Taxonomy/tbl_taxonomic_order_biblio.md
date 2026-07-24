---
table_name: tbl_taxonomic_order_biblio
primary_key: "[[taxonomic_order_biblio_id]]"
foreign_keys:
  - "[[biblio_id]]"
  - "[[taxonomic_order_system_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_biblio]]"
  - "[[tbl_taxonomic_order_systems]]"
---

Contains bibliographic references related to the taxonomic ordering or numbering systems. Multiple references may be associated.
