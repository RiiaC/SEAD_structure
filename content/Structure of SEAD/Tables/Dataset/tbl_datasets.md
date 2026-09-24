---
publish: true
permalink: /Structure of SEAD/Tables/Dataset/tbl_datasets.md
created: 2026-07-24T09:34:40.942Z
modified: 2026-09-24T05:44:40.537Z
published: 2026-09-24T05:44:40.537Z
table_name: tbl_datasets
primary_key: "[[dataset_id]]"
foreign_keys:
  - "[[biblio_id]]"
  - "[[data_type_id]]"
  - "[[master_set_id]]"
  - "[[method_id]]"
  - "[[project_id]]"
  - "[[updated_dataset_id]]"
columns:
  - "[[dataset_name]]"
  - "[[dataset_uuid]]"
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_biblio]]"
  - "[[tbl_data_types]]"
  - "[[tbl_dataset_masters]]"
  - "[[tbl_methods]]"
  - "[[tbl_projects]]"
  - "[[tbl_datasets]]"
date created: Friday, September 19th 2025, 3:37:16 pm
---

Organizes collections of analysis entities into datasets, which are structured collections relevant to the specific proxy being studied. For biological proxies, a dataset typically corresponds to a spreadsheet containing samples and taxa for a single analysis method, such as phosphates through citric acid extraction.
