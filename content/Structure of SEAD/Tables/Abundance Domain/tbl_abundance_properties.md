---
publish: true
permalink: /Structure of SEAD/Tables/Abundance Domain/tbl_abundance_properties.md
created: 2026-11-11T15:17:50.842Z
modified: 2026-11-16T11:23:16.773Z
published: 2026-11-16T11:23:16.773Z
table_name: tbl_abundance_properties
primary_key: "[[abundance_property_id]]"
columns:
  - "[[property_value]]"
connected_tables:
  - "[[tbl_abundances]]"
  - "[[tbl_property_type]]"
foreign_keys:
  - "[[abundance_id]]"
  - "[[property_type_id]]"
role: fact
required: No
domain:
  - abundance
---

> [!abstract] Property/value observation attached to an abundance record.
