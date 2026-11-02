---
publish: true
permalink: /Structure of SEAD/Tables/Dataset/tbl_dataset_submisssions.md
created: 2026-07-24T09:34:40.965Z
modified: 2026-11-02T14:09:03.807Z
published: 2026-11-02T14:09:03.807Z
table_name: tbl_dataset_submissions
primary_key: "[[dataset_submission_id]]"
columns:
  - "[[date_submitted]]"
  - "[[date_updated]]"
  - "[[notes]]"
connected_tables:
  - "[[tbl_contacts]]"
  - "[[tbl_dataset_submission_types]]"
  - "[[tbl_datasets]]"
foreign_keys:
  - "[[contact_id]]"
  - "[[dataset_id]]"
  - "[[submission_type_id]]"
---

Contains records of various submission events related to a dataset, such as initial recording, database entries, and integrations with SEAD.

> [!warning] this table will be depreciated
> Roger let me know in October of 2026 that this table will be depreciated in favour of [[tbl_data_providers]]
