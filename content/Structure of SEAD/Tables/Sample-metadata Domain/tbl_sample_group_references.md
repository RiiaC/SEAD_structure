---
publish: true
permalink: /Structure of SEAD/Tables/Sample-metadata Domain/tbl_sample_group_references.md
created: 2026-07-24T09:34:41.255Z
modified: 2026-11-16T08:33:31.319Z
published: 2026-11-16T08:33:31.319Z
table_name: tbl_sample_group_references
primary_key: "[[sample_group_reference_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_biblio]]"
  - "[[tbl_sample_groups]]"
foreign_keys:
  - "[[biblio_id]]"
  - "[[sample_group_id]]"
---

Contains bibliographic information specifically relevant to a sample group, distinct from site or dataset references (e.g., a publication that reinterprets a structure within a site).
