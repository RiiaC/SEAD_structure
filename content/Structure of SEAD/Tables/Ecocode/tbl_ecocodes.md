---
publish: true
permalink: /Structure of SEAD/Tables/Ecocode/tbl_ecocodes.md
created: 2026-07-24T09:34:41.000Z
modified: 2026-09-23T05:19:09.910Z
published: 2026-09-23T05:19:09.910Z
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
change_it: true
---

Associates ecological classifications with specific taxa.
