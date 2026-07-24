---
table_name: tbl_seasons
primary_key: "[[season_id]]"
foreign_keys:
  - "[[season_type_id]]"
columns:
  - "[[date_updated]]"
  - "[[season_name]]"
  - "[[season_type]]"
  - "[[sort_order]]"
connected_tables:
  - "[[tbl_season_types]]"
---

Contains information about different seasons and their associated months for categorizing activities.
