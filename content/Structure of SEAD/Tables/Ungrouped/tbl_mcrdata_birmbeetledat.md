---
publish: true
permalink: /Structure of SEAD/Tables/Ungrouped/tbl_mcrdata_birmbeetledat.md
created: 2026-07-24T09:34:41.606Z
modified: 2026-09-24T05:44:41.417Z
published: 2026-09-24T05:44:41.417Z
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
---

Stores species climate envelopes using binary 1-degree Celsius cells, categorized by TRange (columns) and TMax (rows). For more information, visit www.bugscep.com.
