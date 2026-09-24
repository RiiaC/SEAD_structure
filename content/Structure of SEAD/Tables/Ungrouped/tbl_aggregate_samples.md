---
publish: true
permalink: /Structure of SEAD/Tables/Ungrouped/tbl_aggregate_samples.md
created: 2026-07-24T09:34:41.506Z
modified: 2026-09-24T05:44:41.313Z
published: 2026-09-24T05:44:41.313Z
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
