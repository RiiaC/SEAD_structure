---
table_name: tbl_mcr_names
primary_key: "[[taxon_id]]"
foreign_keys:
  - "[[taxon_id]]"
columns:
  - "[[comparison_notes]]"
  - "[[date_updated]]"
  - "[[mcr_name_trim]]"
  - "[[mcr_number]]"
  - "[[mcr_species_name]]"
connected_tables:
  - "[[tbl_taxa_tree_master]]"
---

Contains the original taxon names utilized in the Birmingham MCR calculation system for climate reconstruction. It ensures the reproducibility of results and facilitates comparison with historical data.
