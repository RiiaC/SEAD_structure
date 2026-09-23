---
publish: true
permalink: /Structure of SEAD/Tables/Location/tbl_locations.md
created: 2026-07-24T09:34:41.048Z
modified: 2026-09-23T05:19:10.263Z
published: 2026-09-23T05:19:10.263Z
table_name: tbl_locations
primary_key: "[[location_id]]"
foreign_keys:
  - "[[location_type_id]]"
columns:
  - "[[date_updated]]"
  - "[[default_lat_dd]]"
  - "[[default_long_dd]]"
  - "[[location_name]]"
connected_tables:
  - "[[tbl_location_types]]"
date created: Friday, September 19th 2025, 3:37:16 pm
change_it: true
---

Represents geographical locations, typically defined by regions. These can be current or historical locations.
