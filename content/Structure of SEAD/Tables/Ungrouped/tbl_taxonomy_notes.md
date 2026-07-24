---
table_name: tbl_taxonomy_notes
primary_key: "[[taxonomy_notes_id]]"
foreign_keys:
  - "[[biblio_id]]"
  - "[[taxon_id]]"
columns:
  - "[[date_updated]]"
  - "[[taxonomy_notes]]"
  - "[[taxonomy_notes_uuid]]"
connected_tables:
  - "[[tbl_biblio]]"
  - "[[tbl_taxa_tree_master]]"
---

Contains general notes on taxa, primarily regarding identification issues (e.g., potential confusion with similar taxa), and may include references and image links.
