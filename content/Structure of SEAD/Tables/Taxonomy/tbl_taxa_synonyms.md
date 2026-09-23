---
publish: true
permalink: /Structure of SEAD/Tables/Taxonomy/tbl_taxa_synonyms.md
created: 2026-07-24T09:34:41.453Z
modified: 2026-09-23T05:19:12.807Z
published: 2026-09-23T05:19:12.807Z
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
change_it: true
---

Contains alternative scientific names for taxa, along with primary references for their definition or usage.
