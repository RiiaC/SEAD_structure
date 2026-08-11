---
table_name: tbl_relative_ages
primary_key: "[[relative_age_id]]"
foreign_keys:
  - "[[location_id]]"
  - "[[relative_age_type_id]]"
columns:
  - "[[abbreviation]]"
  - "[[c14_age_older]]"
  - "[[c14_age_younger]]"
  - "[[cal_age_older]]"
  - "[[cal_age_younger]]"
  - "[[date_updated]]"
  - "[[source/docs/plugins/Description]]"
  - "[[notes]]"
  - "[[relative_age_name]]"
  - "[[relative_age_uuid]]"
connected_tables:
  - "[[tbl_relative_age_types]]"
  - "[[tbl_locations]]"
date created: Friday, September 19th 2025, 3:37:16 pm
publish: true
---

> [!info] Contains definitions of ages based on historical periods or calendar events, including age ranges and geographical relevance (e.g., Mesolithic in Sweden).

> [!abstract] Additional information, not in the database description of this table, but perhaps it should be:
Relative ages are used to store and search for the interpreted age of a sample or material or site (before present), but not the internal age of an object (e.g. a tree or animal). 
