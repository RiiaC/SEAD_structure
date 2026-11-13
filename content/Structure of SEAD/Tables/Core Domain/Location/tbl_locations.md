---
publish: true
permalink: /Structure of SEAD/Tables/Core Domain/Location/tbl_locations.md
created: 2026-07-24T09:34:41.048Z
modified: 2026-11-03T06:15:47.829Z
published: 2026-11-03T06:15:47.829Z
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
---

Represents geographical locations, typically defined by regions. These can be current or historical locations.
