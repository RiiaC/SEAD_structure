---
table_name: tbl_site_images
primary_key: "[[site_image_id]]"
foreign_keys:
  - "[[contact_id]]"
  - "[[image_type_id]]"
  - "[[site_id]]"
  - "[[tbl_locations]]"
columns:
  - "[[credit]]"
  - "[[date_taken]]"
  - "[[date_updated]]"
  - "[[source/docs/plugins/Description]]"
  - "[[image_location]]"
  - "[[image_name]]"
connected_tables:
  - "[[tbl_contacts]]"
  - "[[tbl_image_types]]"
  - "[[tbl_sites]]"
---

Contains images related to a site, such as site photographs, aerial images, or location maps.
