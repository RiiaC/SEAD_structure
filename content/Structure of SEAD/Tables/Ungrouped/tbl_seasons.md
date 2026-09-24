---
publish: true
permalink: /Structure of SEAD/Tables/Ungrouped/tbl_seasons.md
created: 2026-07-24T09:34:41.645Z
modified: 2026-09-24T05:44:41.434Z
published: 2026-09-24T05:44:41.434Z
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
