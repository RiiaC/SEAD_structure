---
publish: true
permalink: /Structure of SEAD/Tables/Taxonomy/tbl_taxa_seasonality.md
created: 2026-07-24T09:34:41.451Z
modified: 2026-09-23T05:19:12.807Z
published: 2026-09-23T05:19:12.807Z
table_name: tbl_taxa_seasonality
primary_key: "[[seasonality_id]]"
foreign_keys:
  - "[[activity_type_id]]"
  - "[[location_id]]"
  - "[[season_id]]"
  - "[[taxon_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_activity_types]]"
  - "[[tbl_seasons]]"
  - "[[tbl_taxa_tree_master]]"
  - "[[tbl_locations]]"
date created: Friday, September 19th 2025, 3:37:16 pm
change_it: true
---

Contains information about the specific parts of the year (e.g., Winter, June) during which certain activities or developmental stages of taxa occur (e.g., adult stage from June to August).
