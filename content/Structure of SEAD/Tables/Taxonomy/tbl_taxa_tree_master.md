---
publish: true
permalink: /Structure of SEAD/Tables/Taxonomy/tbl_taxa_tree_master.md
created: 2026-07-24T09:34:41.475Z
modified: 2026-10-02T09:16:37.412Z
published: 2026-10-02T09:16:37.412Z
table_name: "[[tbl_taxa_tree_master]]"
primary_key: "[[taxon_id]]"
columns:
  - "[[date_updated]]"
  - "[[species]]"
connected_tables:
  - "[[tbl_taxa_tree_authors]]"
  - "[[tbl_taxa_tree_genera]]"
foreign_keys:
  - "[[author_id]]"
  - "[[genus_id]]"
url: https://humlab-sead.github.io/sead-schema/tables/tbl_taxa_tree_master.html
---

Represents the finest level of taxonomic classification, typically at the species level. It may also include designations such as 'sp.' for an unspecified single species, 'spp.' for multiple unspecified species, 'grp' for taxonomic groups, or split identifications (e.g., x/y), along with other cases depending on the taxonomic context.
