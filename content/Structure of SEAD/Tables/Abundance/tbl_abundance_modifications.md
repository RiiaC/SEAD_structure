---
publish: true
permalink: /Structure of SEAD/Tables/Abundance/tbl_abundance_modifications.md
created: 2026-07-24T09:34:41.411Z
modified: 2026-11-11T15:17:48.491Z
published: 2026-11-11T15:17:48.491Z
table_name: tbl_abundance_modifications
primary_key: "[[abundance_modification_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_abundances]]"
  - "[[tbl_modification_types]]"
foreign_keys:
  - "[[abundance_id]]"
  - "[[modification_type_id]]"
Role: fact
---

Contains information about modifications applied to individual specimen counts, such as carbonization, corrosion, or calcification. This enables recording multiple instances of the same taxon with varying modifications (e.g., Hordeum sp. carbonized and Hordeum sp. unmodified).
