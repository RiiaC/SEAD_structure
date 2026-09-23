---
publish: true
permalink: /Structure of SEAD/Tables/Analysis Entities/tbl_analysis_entities.md
created: 2026-07-24T09:34:40.937Z
modified: 2026-09-23T05:19:09.630Z
published: 2026-09-23T05:19:09.630Z
table_name: tbl_analysis_entities
primary_key: "[[analysis_entity_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_datasets]]"
  - "[[tbl_physical_samples]]"
foreign_keys:
  - "[[dataset_id]]"
  - "[[physical_sample_id]]"
date created: Friday, September 19th 2025, 3:37:16 pm
change_it: true
---

> [!info] Represents analysis entities, which are virtual constructs allowing the association of multiple proxies with a single physical sample. This enables the linking of physical samples to various measurements or counts across different methods. Analysis Entities are organized by datasets, which are constructed based on proxy requirements. Refer to the 'Dataset' documentation for more details.
