---
publish: true
permalink: /Structure of SEAD/Tables/Sample Groups/tbl_sample_group_references.md
created: 2026-07-24T09:34:41.255Z
modified: 2026-09-24T05:44:41.046Z
published: 2026-09-24T05:44:41.046Z
table_name: tbl_sample_group_references
primary_key: "[[sample_group_reference_id]]"
foreign_keys:
  - "[[biblio_id]]"
  - "[[sample_group_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_biblio]]"
  - "[[tbl_sample_groups]]"
---

Contains bibliographic information specifically relevant to a sample group, distinct from site or dataset references (e.g., a publication that reinterprets a structure within a site).
