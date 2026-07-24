---
table_name: tbl_taxa_images
primary_key: "[[taxa_images_id]]"
foreign_keys:
  - "[[image_type_id]]"
  - "[[taxon_id]]"
columns:
  - "[[date_updated]]"
  - "[[source/docs/plugins/Description]]"
  - "[[image_location]]"
  - "[[image_name]]"
connected_tables:
  - "[[tbl_image_types]]"
  - "[[tbl_taxa_tree_master]]"
---

Contains references to images of taxa, stored either in external databases or available online.
