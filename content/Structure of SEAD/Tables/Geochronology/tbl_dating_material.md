---
publish: true
permalink: /Structure of SEAD/Tables/Geochronology/tbl_dating_material.md
created: 2026-07-24T09:34:41.543Z
modified: 2026-09-24T05:44:40.680Z
published: 2026-09-24T05:44:40.680Z
table_name: tbl_dating_material
primary_key: "[[dating_material_id]]"
foreign_keys:
  - "[[abundance_element_id]]"
  - "[[geochron_id]]"
  - "[[taxon_id]]"
columns:
  - "[[date_updated]]"
  - "[[description]]"
  - "[[material_dated]]"
connected_tables:
  - "[[tbl_abundance_elements]]"
  - "[[tbl_geochronology]]"
  - "[[tbl_taxa_tree_master]]"
date created: Friday, September 19th 2025, 3:37:16 pm
---

Contains information about materials used for dating processes. Materials can be linked to a specific taxon, pseudotaxon, or described in the 'material\_dated' field. Specific components of abundance, such as seeds or elytrons, can also be indicated. A single dating instance may involve multiple materials.
