---
publish: true
permalink: /Structure of SEAD/Tables/Sites/tbl_site_locations.md
created: 2026-07-24T09:34:41.288Z
modified: 2026-09-23T05:19:10.997Z
published: 2026-09-23T05:19:10.997Z
table_name: tbl_site_locations
primary_key: "[[site_location_id]]"
foreign_keys:
  - "[[location_id]]"
  - "[[site_id]]"
  - "[[tbl_locations]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_sites]]"
  - "[[tbl_locations]]"
date created: Friday, September 19th 2025, 3:37:16 pm
change_it: true
---

Associates site identifiers with location names.

> [!info] to add somewhere
> only geographical objects like socken, by, counties, lakes, regions etc. Archaeological site is not used as a location type in this context, or at least should not be...
