---
publish: true
permalink: /Structure of SEAD/Tables/Geochronology/tbl_dating_material.md
created: 2026-07-24T09:34:41.543Z
modified: 2026-10-02T09:16:36.988Z
published: 2026-10-02T09:16:36.988Z
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
---

Contains information about materials used for dating processes. Materials can be linked to a specific taxon, pseudotaxon, or described in the 'material\_dated' field. Specific components of abundance, such as seeds or elytrons, can also be indicated. A single dating instance may involve multiple materials.
