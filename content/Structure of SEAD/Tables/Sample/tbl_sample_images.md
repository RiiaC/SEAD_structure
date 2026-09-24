---
publish: true
permalink: /Structure of SEAD/Tables/Sample/tbl_sample_images.md
created: 2026-07-24T09:34:41.363Z
modified: 2026-09-24T05:44:40.979Z
published: 2026-09-24T05:44:40.979Z
table_name: tbl_sample_images
primary_key: "[[sample_image_id]]"
foreign_keys:
  - "[[image_type_id]]"
  - "[[physical_sample_id]]"
columns:
  - "[[date_updated]]"
  - "[[description]]"
  - "[[image_location]]"
  - "[[image_name]]"
connected_tables:
  - "[[tbl_image_types]]"
  - "[[tbl_physical_samples]]"
---

Contains images related to samples, including site photographs, lab processing images, and microscope images.
