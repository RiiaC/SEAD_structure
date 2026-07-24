---
table_name: tbl_sample_group_images
primary_key: "[[sample_group_image_id]]"
foreign_keys:
  - "[[image_type_id]]"
  - "[[sample_group_id]]"
columns:
  - "[[date_updated]]"
  - "[[source/docs/plugins/Description]]"
  - "[[image_location]]"
  - "[[image_name]]"
connected_tables:
  - "[[tbl_image_types]]"
  - "[[tbl_sample_groups]]"
---

Contains images related to sample groups, such as photographs or annotated sketches of cores.
