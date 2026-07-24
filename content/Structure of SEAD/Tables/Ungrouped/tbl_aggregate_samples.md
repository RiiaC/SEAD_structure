---
table_name: tbl_aggregate_samples
primary_key: "[[aggregate_sample_id]]"
foreign_keys:
  - "[[aggregate_dataset_id]]"
  - "[[analysis_entity_id]]"
columns:
  - "[[aggregate_sample_name]]"
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_aggregate_datasets]]"
  - "[[tbl_analysis_entities]]"
---

20120504pib: can we drop aggregate sample name? seems excessive and unnecessary sample names can be traced.
