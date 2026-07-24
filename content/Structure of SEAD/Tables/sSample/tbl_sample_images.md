---
table_name: tbl_sample_images
primary_key: "[[sample_image_id]]"
foreign_keys:
  - "[[image_type_id]]"
  - "[[physical_sample_id]]"
columns:
  - "[[date_updated]]"
  - "[[source/docs/plugins/Description]]"
  - "[[image_location]]"
  - "[[image_name]]"
connected_tables:
  - "[[tbl_image_types]]"
  - "[[tbl_physical_samples]]"
---

Contains images related to samples, including site photographs, lab processing images, and microscope images.
