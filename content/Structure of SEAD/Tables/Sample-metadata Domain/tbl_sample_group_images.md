---
publish: true
permalink: /Structure of SEAD/Tables/Sample-metadata Domain/tbl_sample_group_images.md
created: 2026-07-24T09:34:41.247Z
modified: 2026-11-16T12:46:46.176Z
published: 2026-11-16T12:46:46.176Z
table_name: tbl_sample_group_images
primary_key: "[[sample_group_image_id]]"
columns:
  - "[[date_updated]]"
  - "[[description]]"
  - "[[image_location]]"
  - "[[image_name]]"
connected_tables:
  - "[[tbl_image_types]]"
  - "[[tbl_sample_groups]]"
foreign_keys:
  - "[[image_type_id]]"
  - "[[sample_group_id]]"
---

Contains images related to sample groups, such as photographs or annotated sketches of cores.
