---
table_name: tbl_ecocode_definitions
primary_key: "[[ecocode_definition_id]]"
foreign_keys:
  - "[[ecocode_group_id]]"
columns:
  - "[[abbreviation]]"
  - "[[date_updated]]"
  - "[[definition]]"
  - "[[name]]"
  - "[[notes]]"
  - "[[sort_order]]"
connected_tables:
  - "[[tbl_ecocode_groups]]"
date created: Friday, September 19th 2025, 3:37:16 pm
---

Contains definitions for ecological, habitat, or ethnographic categories, which are linked to specific taxa within a defined classification system.
