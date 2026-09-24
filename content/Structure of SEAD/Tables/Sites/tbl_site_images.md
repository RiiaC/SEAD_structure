---
publish: true
permalink: /Structure of SEAD/Tables/Sites/tbl_site_images.md
created: 2026-07-24T09:34:41.282Z
modified: 2026-09-24T05:44:41.101Z
published: 2026-09-24T05:44:41.101Z
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
  - "[[description]]"
  - "[[image_location]]"
  - "[[image_name]]"
connected_tables:
  - "[[tbl_contacts]]"
  - "[[tbl_image_types]]"
  - "[[tbl_sites]]"
---

Contains images related to a site, such as site photographs, aerial images, or location maps.
