---
table_name: "[[tbl_sample_alt_refs]]"
primary_key: "[[sample_alt_ref_id]]"
foreign_keys:
  - "[[alt_ref_type_id]]"
  - "[[physical_sample_id]]"
columns:
  - "[[alt_ref]]"
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_alt_ref_types]]"
  - "[[tbl_physical_samples]]"
date created: Friday, September 19th 2025, 3:37:16 pm
publish: true
---

Contains various reference names for physical samples, such as laboratory or field numbers.
