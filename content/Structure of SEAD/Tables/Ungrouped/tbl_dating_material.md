---
table_name: tbl_dating_material
primary_key: "[[dating_material_id]]"
foreign_keys:
  - "[[abundance_element_id]]"
  - "[[geochron_id]]"
  - "[[taxon_id]]"
columns:
  - "[[date_updated]]"
  - "[[source/docs/plugins/Description]]"
  - "[[material_dated]]"
connected_tables:
  - "[[tbl_abundance_elements]]"
  - "[[tbl_geochronology]]"
  - "[[tbl_taxa_tree_master]]"
date created: Friday, September 19th 2025, 3:37:16 pm
---

Contains information about materials used for dating processes. Materials can be linked to a specific taxon, pseudotaxon, or described in the 'material_dated' field. Specific components of abundance, such as seeds or elytrons, can also be indicated. A single dating instance may involve multiple materials.
