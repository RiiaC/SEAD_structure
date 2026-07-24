---
table_name: tbl_taxa_synonyms
primary_key: "[[synonym_id]]"
foreign_keys:
  - "[[author_id]]"
  - "[[biblio_id]]"
  - "[[family_id]]"
  - "[[genus_id]]"
  - "[[taxon_id]]"
columns:
  - "[[date_updated]]"
  - "[[notes]]"
  - "[[reference_type]]"
  - "[[synonym]]"
  - "[[synonym_uuid]]"
connected_tables:
  - "[[tbl_taxa_tree_authors]]"
  - "[[tbl_biblio]]"
  - "[[tbl_taxa_tree_families]]"
  - "[[tbl_taxa_tree_genera]]"
  - "[[tbl_taxa_tree_master]]"
date created: Friday, September 19th 2025, 3:37:16 pm
---

Contains alternative scientific names for taxa, along with primary references for their definition or usage.
