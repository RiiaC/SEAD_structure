---
publish: true
permalink: /Structure of SEAD/Tables/Ungrouped/tbl_text_identification_keys.md
created: 2026-07-24T09:34:41.681Z
modified: 2026-09-23T05:19:12.642Z
published: 2026-09-23T05:19:12.642Z
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
change_it: true
---

Stores identification key extracts along with their bibliographic sources.
