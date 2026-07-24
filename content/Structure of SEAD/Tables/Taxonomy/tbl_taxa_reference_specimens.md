---
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
---

Contains information on reference and type specimens used for the primary description of species.
