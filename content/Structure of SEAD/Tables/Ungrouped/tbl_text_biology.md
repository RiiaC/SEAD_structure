---
table_name: tbl_text_biology
primary_key: "[[biology_id]]"
foreign_keys:
  - "[[biblio_id]]"
  - "[[taxon_id]]"
columns:
  - "[[biology_text]]"
  - "[[biology_uuid]]"
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_biblio]]"
  - "[[tbl_taxa_tree_master]]"
---

Contains ecological, habitat, and behavioral information for various taxa, along with references to their sources, such as 'in hollows on old oaks.'
