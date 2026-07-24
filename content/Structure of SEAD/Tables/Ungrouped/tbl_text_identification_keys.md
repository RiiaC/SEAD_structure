---
table_name: tbl_text_identification_keys
primary_key: "[[key_id]]"
foreign_keys:
  - "[[biblio_id]]"
  - "[[taxon_id]]"
columns:
  - "[[date_updated]]"
  - "[[key_text]]"
  - "[[key_uuid]]"
connected_tables:
  - "[[tbl_biblio]]"
  - "[[tbl_taxa_tree_master]]"
---

Stores identification key extracts along with their bibliographic sources.
