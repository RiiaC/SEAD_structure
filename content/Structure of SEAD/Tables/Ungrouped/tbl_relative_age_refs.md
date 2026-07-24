---
table_name: tbl_relative_age_refs
primary_key: "[[relative_age_ref_id]]"
foreign_keys:
  - "[[biblio_id]]"
  - "[[relative_age_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_biblio]]"
  - "[[tbl_relative_ages]]"
---

Stores bibliographic references that define the accepted authority for a dating period, rather than the dating of a specific sample.
