---
table_name: tbl_analysis_taxon_counts
primary_key: "[[analysis_taxon_count_id]]"
foreign_keys:
  - "[[analysis_value_id]]"
  - "[[taxon_id]]"
columns:
  - "[[value]]"
connected_tables:
  - "[[tbl_analysis_values]]"
  - "[[tbl_taxa_tree_master]]"
date created: Friday, September 19th 2025, 3:37:16 pm
---

Storage for analysis values that represents a taxon counts.
