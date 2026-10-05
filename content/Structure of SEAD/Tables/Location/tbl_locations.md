---
publish: true
permalink: /Structure of SEAD/Tables/Location/tbl_locations.md
created: 2026-07-24T09:34:41.048Z
modified: 2026-10-02T09:16:37.111Z
published: 2026-10-02T09:16:37.111Z
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
---

Represents geographical locations, typically defined by regions. These can be current or historical locations.
