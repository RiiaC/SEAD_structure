---
table_name: tbl_sample_descriptions
primary_key: "[[sample_description_id]]"
foreign_keys:
  - "[[physical_sample_id]]"
  - "[[sample_description_type_id]]"
columns:
  - "[[date_updated]]"
  - "[[Structure of SEAD/Columns/description|description]]"
connected_tables:
  - "[[tbl_physical_samples]]"
  - "[[tbl_sample_description_types]]"
date created: Friday, September 19th 2025, 3:37:16 pm
publish: true
---

Contains detailed descriptions of samples categorized by different description types.
