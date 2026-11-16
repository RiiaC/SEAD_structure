---
publish: true
permalink: /Structure of SEAD/Tables/Ungrouped/core/tbl_datasets.md
created: 2026-07-24T09:34:40.942Z
modified: 2026-11-16T12:30:23.945Z
published: 2026-11-16T12:30:23.945Z
table_name: tbl_datasets
primary_key: "[[dataset_id]]"
columns:
  - "[[dataset_name]]"
  - "[[dataset_uuid]]"
  - "[[date_updated]]"
foreign_keys:
  - "[[biblio_id]]"
  - "[[data_type_id]]"
  - "[[master_set_id]]"
  - "[[method_id]]"
  - "[[project_id]]"
  - "[[updated_dataset_id]]"
connected_tables:
  - "[[tbl_analysis_entities]]"
  - "[[tbl_biblio]]"
  - "[[tbl_data_types]]"
  - "[[tbl_dataset_contacts]]"
  - "[[tbl_dataset_masters]]"
  - "[[tbl_dataset_submisssions]]"
  - "[[tbl_datasets]]"
  - "[[tbl_methods]]"
  - "[[tbl_projects]]"
required: No
role: lookup
domain:
  - core
---

> [!abstract] Dataset context for imported analytical observations.
> Organizes collections of analysis entities into datasets, which are structured collections relevant to the specific proxy being studied. For biological proxies, a dataset typically corresponds to a spreadsheet containing samples and taxa for a single analysis method, such as phosphates through citric acid extraction.
