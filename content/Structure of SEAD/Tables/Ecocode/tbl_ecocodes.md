---
table_name: tbl_ecocodes
primary_key: "[[ecocode_id]]"
foreign_keys:
  - "[[ecocode_definition_id]]"
  - "[[taxon_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_ecocode_definitions]]"
  - "[[tbl_taxa_tree_master]]"
---

Associates ecological classifications with specific taxa.
