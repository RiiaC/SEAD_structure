---
publish: true
permalink: /Structure of SEAD/Tables/Ungrouped/tbl_mcrdata_birmbeetledat.md
created: 2026-07-24T09:34:41.606Z
modified: 2026-09-23T05:19:12.507Z
published: 2026-09-23T05:19:12.507Z
table_name: tbl_mcrdata_birmbeetledat
primary_key: "[[mcrdata_birmbeetledat_id]]"
foreign_keys:
  - "[[taxon_id]]"
columns:
  - "[[date_updated]]"
  - "[[mcr_data]]"
  - "[[mcr_row]]"
connected_tables:
  - "[[tbl_taxa_tree_master]]"
change_it: true
---

Stores species climate envelopes using binary 1-degree Celsius cells, categorized by TRange (columns) and TMax (rows). For more information, visit www.bugscep.com.
