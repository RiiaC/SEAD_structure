---
publish: true
permalink: /Structure of SEAD/Tables/Abundance Domain/tbl_abundance_properties.md
created: 2026-11-11T15:17:50.842Z
modified: 2026-11-16T14:08:57.933Z
published: 2026-11-16T14:08:57.933Z
table_name: tbl_abundance_properties
primary_key: "[[abundance_property_id]]"
columns:
  - "[[property_value]]"
foreign_keys:
  - "[[abundance_id]]"
  - "[[property_type_id]]"
connected_tables:
  - "[[tbl_abundances]]"
  - "[[tbl_property_type]]"
required: No
role: fact
domain:
  - abundance
---

> [!abstract] Property/value observation attached to an abundance record.
