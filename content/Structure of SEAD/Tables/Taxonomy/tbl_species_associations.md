---
publish: true
permalink: /Structure of SEAD/Tables/Taxonomy/tbl_species_associations.md
created: 2026-07-24T09:34:41.424Z
modified: 2026-09-23T05:19:12.758Z
published: 2026-09-23T05:19:12.758Z
table_name: tbl_species_associations
primary_key: "[[species_association_id]]"
foreign_keys:
  - "[[association_type_id]]"
  - "[[biblio_id]]"
  - "[[taxon_id]]"
columns:
  - "[[associated_taxon_id]]"
  - "[[date_updated]]"
  - "[[referencing_type]]"
  - "[[species_association_uuid]]"
connected_tables:
  - "[[tbl_species_association_types]]"
  - "[[tbl_biblio]]"
  - "[[tbl_taxa_tree_master]]"
date created: Friday, September 19th 2025, 3:37:16 pm
change_it: true
---

Represents the relationships between different taxa, including interactions such as predation, parasitism, shared habitats, and synonym links. The directionality of the association (e.g., 'x preys on y') is crucial.
