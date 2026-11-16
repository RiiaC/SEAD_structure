---
publish: true
permalink: /Structure of SEAD/Tables/Core Domain/also in Spatial/tbl_site_locations.md
created: 2026-07-24T09:34:41.288Z
modified: 2026-11-16T10:14:33.049Z
published: 2026-11-16T10:14:33.049Z
table_name: tbl_site_locations
primary_key: "[[site_location_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_locations]]"
  - "[[tbl_sites]]"
foreign_keys:
  - "[[location_id]]"
  - "[[site_id]]"
  - "[[tbl_locations]]"
required: Yes
role: bridge
domain:
  - core
  - spatial
---

> [!abstract] Join entity connecting sites to locations, allowing for many-to-many relationships between the two.
> Associates site identifiers with location names.

> [!Note]
> only geographical objects like socken, by, counties, lakes, regions etc. Archaeological site is not used as a location type in this context, or at least should not be...
