---
publish: true
permalink: /Structure of SEAD/Tables/Taxonomy/tbl_taxa_reference_specimens.md
created: 2026-07-24T09:34:41.445Z
modified: 2026-09-23T05:19:12.789Z
published: 2026-09-23T05:19:12.789Z
table_name: tbl_taxa_reference_specimens
primary_key: "[[taxa_reference_specimen_id]]"
foreign_keys:
  - "[[contact_id]]"
  - "[[taxon_id]]"
columns:
  - "[[date_updated]]"
  - "[[notes]]"
connected_tables:
  - "[[tbl_contacts]]"
  - "[[tbl_taxa_tree_master]]"
change_it: true
---

Contains information on reference and type specimens used for the primary description of species.
