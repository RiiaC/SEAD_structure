---
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
---

Represents the relationships between different taxa, including interactions such as predation, parasitism, shared habitats, and synonym links. The directionality of the association (e.g., 'x preys on y') is crucial.
