---
publish: true
permalink: /Structure of SEAD/Tables/Taxa Counts/tbl_abundance_ident_levels.md
created: 2026-07-24T09:34:41.405Z
modified: 2026-10-02T09:16:37.327Z
published: 2026-10-02T09:16:37.327Z
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
---

Represents the degree of certainty in taxonomic identification, categorized by levels such as Family, Genus, or Species (e.g., cf. Family, cf. Genus, cf. Species).
