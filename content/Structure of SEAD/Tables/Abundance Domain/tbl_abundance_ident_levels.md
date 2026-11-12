---
publish: true
permalink: /Structure of SEAD/Tables/Abundance Domain/tbl_abundance_ident_levels.md
created: 2026-07-24T09:34:41.405Z
modified: 2026-11-11T16:12:28.111Z
published: 2026-11-11T16:12:28.111Z
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
role: bridge
domain:
  - abundance
  - taxonomy
required: No
---

> [!info] Links abundance records to identification confidence levels
> Represents the degree of certainty in taxonomic identification, categorised by levels such as Family, Genus, or Species (e.g., cf. Family, cf. Genus, cf. Species).
