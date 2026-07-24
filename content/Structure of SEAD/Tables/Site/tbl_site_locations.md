---
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
---
Associates site identifiers with location names.

> [!info] to add somewhere
> only geographical objects like socken, by, counties, lakes, regions etc. Archaeological site is not used as a location type in this context, or at least should not be...



