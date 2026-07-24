---
table_name: tbl_aggregate_sample_ages
primary_key: "[[aggregate_sample_age_id]]"
foreign_keys:
  - "[[aggregate_dataset_id]]"
  - "[[analysis_entity_age_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_aggregate_datasets]]"
  - "[[tbl_analysis_entity_ages]]"
---

nan
