---
publish: true
permalink: /Structure of SEAD/Tables/Taxa Counts/tbl_abundance_ident_levels.md
created: 2026-07-24T09:34:41.405Z
modified: 2026-09-23T05:19:11.405Z
published: 2026-09-23T05:19:11.405Z
table_name: tbl_abundance_ident_levels
primary_key: "[[abundance_ident_level_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_abundances]]"
  - "[[tbl_identification_levels]]"
foreign_keys:
  - "[[abundance_id]]"
  - "[[identification_level_id]]"
date created: Friday, September 19th 2025, 3:37:16 pm
change_it: true
---

Represents the degree of certainty in taxonomic identification, categorized by levels such as Family, Genus, or Species (e.g., cf. Family, cf. Genus, cf. Species).
