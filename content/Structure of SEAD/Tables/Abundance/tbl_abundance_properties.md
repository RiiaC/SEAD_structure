---
publish: true
permalink: /Structure of SEAD/Tables/Abundance/tbl_abundance_properties.md
created: 2026-11-11T15:17:50.842Z
modified: 2026-11-11T16:46:06.099Z
published: 2026-11-11T16:46:06.099Z
table_name: tbl_abundance_properties
primary_key: "[[abundance_property_id]]"
columns:
connected_tables:
foreign_keys:
  - "[[abundance_id]]"
  - "[[property_type_id]]"
role: fact
required: No
domain:
  - abundance
---

> [!abstract] Property/value observation attached to an abundance record.

A new table created autumn 2026

- [ ] Add the columns and connections as soon as you have access
