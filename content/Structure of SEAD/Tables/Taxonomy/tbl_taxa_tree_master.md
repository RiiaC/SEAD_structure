---
table_name: "[[tbl_taxa_tree_master]]"
primary_key: "[[taxon_id]]"
foreign_keys:
  - "[[author_id]]"
  - "[[genus_id]]"
columns:
  - "[[date_updated]]"
  - "[[species]]"
connected_tables:
  - "[[tbl_taxa_tree_authors]]"
  - "[[tbl_taxa_tree_genera]]"
date created: Friday, September 19th 2025, 3:37:16 pm
url: https://humlab-sead.github.io/sead-schema/tables/tbl_taxa_tree_master.html
---

Represents the finest level of taxonomic classification, typically at the species level. It may also include designations such as 'sp.' for an unspecified single species, 'spp.' for multiple unspecified species, 'grp' for taxonomic groups, or split identifications (e.g., x/y), along with other cases depending on the taxonomic context.


