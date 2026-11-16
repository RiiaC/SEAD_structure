---
publish: true
permalink: /Structure of SEAD/Tables/Core Domain/also in Spatial/tbl_locations.md
created: 2026-07-24T09:34:41.048Z
modified: 2026-11-16T08:38:37.010Z
published: 2026-11-16T08:38:37.010Z
table_name: tbl_locations
primary_key: "[[location_id]]"
columns:
  - "[[date_updated]]"
  - "[[default_lat_dd]]"
  - "[[default_long_dd]]"
  - "[[location_name]]"
connected_tables:
  - "[[tbl_location_types]]"
foreign_keys:
  - "[[location_type_id]]"
required: Yes
role: lookup
domain:
  - core
  - spatial
---

> [!abstract] Geographic location referenced by sites and other context entities.
> Represents geographical locations, typically defined by regions. These can be current or historical locations.
