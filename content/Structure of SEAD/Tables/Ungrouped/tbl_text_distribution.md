---
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
---

Contains descriptive distribution information for taxa, along with references to the source publications. For example, 'Scandinavia north of Tromsø, British Isles - rare.'
