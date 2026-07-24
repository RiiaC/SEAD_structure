---
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
---

Represents geographical locations, typically defined by regions. These can be current or historical locations.
