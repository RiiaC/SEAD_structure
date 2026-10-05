---
publish: true
permalink: /Structure of SEAD/Tables/Dataset/tbl_datasets.md
created: 2026-07-24T09:34:40.942Z
modified: 2026-10-02T09:16:36.871Z
published: 2026-10-02T09:16:36.871Z
table_name: tbl_datasets
primary_key: "[[dataset_id]]"
columns:
  - "[[dataset_name]]"
  - "[[dataset_uuid]]"
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_biblio]]"
  - "[[tbl_data_types]]"
  - "[[tbl_dataset_masters]]"
  - "[[tbl_datasets]]"
  - "[[tbl_methods]]"
  - "[[tbl_projects]]"
foreign_keys:
  - "[[biblio_id]]"
  - "[[data_type_id]]"
  - "[[master_set_id]]"
  - "[[method_id]]"
  - "[[project_id]]"
  - "[[updated_dataset_id]]"
---

Organizes collections of analysis entities into datasets, which are structured collections relevant to the specific proxy being studied. For biological proxies, a dataset typically corresponds to a spreadsheet containing samples and taxa for a single analysis method, such as phosphates through citric acid extraction.
