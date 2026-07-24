---
table_name: tbl_ecocode_groups
primary_key: "[[ecocode_group_id]]"
foreign_keys:
  - "[[ecocode_system_id]]"
columns:
  - "[[abbreviation]]"
  - "[[date_updated]]"
  - "[[definition]]"
  - "[[name]]"
connected_tables:
  - "[[tbl_ecocode_systems]]"
---

Represents a hierarchical classification system for taxon groups, allowing integration of diverse classification types such as habitat, food type, and food condition.
