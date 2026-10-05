---
publish: true
permalink: /Structure of SEAD/Tables/Ecocode/tbl_ecocode_definitions.md
created: 2026-07-24T09:34:41.000Z
modified: 2026-10-02T09:16:36.962Z
published: 2026-10-02T09:16:36.962Z
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
---

Contains definitions for ecological, habitat, or ethnographic categories, which are linked to specific taxa within a defined classification system.
