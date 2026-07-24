---
table_name: tbl_tephra_refs
primary_key: "[[tephra_ref_id]]"
foreign_keys:
  - "[[biblio_id]]"
  - "[[tephra_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_biblio]]"
  - "[[tbl_tephras]]"
---

Contains bibliographic information related to the identification and description of tephra layers (volcanic ash deposits).
