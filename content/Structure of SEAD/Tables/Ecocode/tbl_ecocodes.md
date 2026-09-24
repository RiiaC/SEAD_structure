---
publish: true
permalink: /Structure of SEAD/Tables/Ecocode/tbl_ecocodes.md
created: 2026-07-24T09:34:41.000Z
modified: 2026-09-24T05:44:40.637Z
published: 2026-09-24T05:44:40.637Z
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
