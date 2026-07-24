---
table_name: tbl_taxa_tree_families
primary_key: "[[family_id]]"
foreign_keys:
  - "[[order_id]]"
columns:
  - "[[date_updated]]"
  - "[[family_name]]"
connected_tables:
  - "[[tbl_taxa_tree_orders]]"
date created: Friday, September 19th 2025, 3:37:16 pm
---

Specifies information about taxonomic families.
