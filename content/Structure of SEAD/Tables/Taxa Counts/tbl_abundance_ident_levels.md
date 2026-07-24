---
table_name: tbl_abundance_ident_levels
primary_key: "[[abundance_ident_level_id]]"
foreign_keys:
  - "[[abundance_id]]"
  - "[[identification_level_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_abundances]]"
  - "[[tbl_identification_levels]]"
date created: Friday, September 19th 2025, 3:37:16 pm
---

Represents the degree of certainty in taxonomic identification, categorized by levels such as Family, Genus, or Species (e.g., cf. Family, cf. Genus, cf. Species).
