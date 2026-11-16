---
publish: true
permalink: /Structure of SEAD/Tables/Analysis Domain/tbl_analysis_entities.md
created: 2026-07-24T09:34:40.937Z
modified: 2026-11-16T12:29:32.168Z
published: 2026-11-16T12:29:32.168Z
table_name: tbl_analysis_entities
primary_key: "[[analysis_entity_id]]"
columns:
  - "[[date_updated]]"
foreign_keys:
  - "[[dataset_id]]"
  - "[[physical_sample_id]]"
connected_tables:
  - "[[tbl_datasets]]"
  - "[[tbl_physical_samples]]"
required: Yes
role: fact
domain:
  - analysis
  - core
---

> [!abstract] Analytical observation context connecting sample and dataset.
> Represents analysis entities, which are virtual constructs allowing the association of multiple proxies with a single physical sample. This enables the linking of physical samples to various measurements or counts across different methods. Analysis Entities are organized by datasets, which are constructed based on proxy requirements. Refer to the 'Dataset' documentation for more details.
