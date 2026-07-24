---
table_name: tbl_taxa_measured_attributes
primary_key: "[[measured_attribute_id]]"
foreign_keys:
  - "[[taxon_id]]"
columns:
  - "[[attribute_measure]]"
  - "[[attribute_type]]"
  - "[[attribute_units]]"
  - "[[data]]"
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_taxa_tree_master]]"
---

Contains measurements related to the size of organisms, such as maximum length.
