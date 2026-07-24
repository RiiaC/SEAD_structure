---
table_name: tbl_taxa_common_names
primary_key: "[[taxon_common_name_id]]"
foreign_keys:
  - "[[language_id]]"
  - "[[taxon_id]]"
columns:
  - "[[common_name]]"
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_languages]]"
  - "[[tbl_taxa_tree_master]]"
date created: Friday, September 19th 2025, 3:37:16 pm
---

Stores vernacular or common names of organisms, such as 'bluebottle'.
