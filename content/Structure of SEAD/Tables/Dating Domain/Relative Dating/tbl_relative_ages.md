---
publish: true
permalink: /Structure of SEAD/Tables/Dating Domain/Relative Dating/tbl_relative_ages.md
created: 2026-07-24T09:34:41.196Z
modified: 2026-11-16T13:41:00.277Z
published: 2026-11-16T13:41:00.277Z
table_name: tbl_relative_ages
primary_key: "[[relative_age_id]]"
columns:
  - "[[abbreviation]]"
  - "[[c14_age_older]]"
  - "[[c14_age_younger]]"
  - "[[cal_age_older]]"
  - "[[cal_age_younger]]"
  - "[[date_updated]]"
  - "[[description]]"
  - "[[notes]]"
  - "[[relative_age_name]]"
  - "[[relative_age_uuid]]"
foreign_keys:
  - "[[location_id]]"
  - "[[relative_age_type_id]]"
connected_tables:
  - "[[tbl_locations]]"
  - "[[tbl_relative_age_types]]"
required: No
role: lookup
domain:
  - dating
---

> [!abstract] Controlled relative-age vocabulary used by archaeological dating records.
> Contains definitions of ages based on historical periods or calendar events, including age ranges and geographical relevance (e.g., Mesolithic in Sweden).

> [!note] Additional information, not in the database description of this table, but perhaps it should be:
> Relative ages are used to store and search for the interpreted age of a sample or material or site (before present), but not the internal age of an object (e.g. a tree or animal).
