---
publish: true
permalink: /Structure of SEAD/Tables/Ungrouped/tbl_text_distribution.md
created: 2026-07-24T09:34:41.681Z
modified: 2026-09-23T05:19:12.623Z
published: 2026-09-23T05:19:12.623Z
table_name: tbl_text_distribution
primary_key: "[[distribution_id]]"
foreign_keys:
  - "[[biblio_id]]"
  - "[[taxon_id]]"
columns:
  - "[[date_updated]]"
  - "[[distribution_text]]"
  - "[[distribution_uuid]]"
connected_tables:
  - "[[tbl_biblio]]"
  - "[[tbl_taxa_tree_master]]"
change_it: true
---

Contains descriptive distribution information for taxa, along with references to the source publications. For example, 'Scandinavia north of Tromsø, British Isles - rare.'
