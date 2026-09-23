---
publish: true
permalink: /Structure of SEAD/Tables/Dataset/tbl_dataset_submisssion.md
created: 2026-07-24T09:34:40.965Z
modified: 2026-09-23T05:19:09.846Z
published: 2026-09-23T05:19:09.846Z
table_name: tbl_dataset_submissions
primary_key: "[[dataset_submission_id]]"
foreign_keys:
  - "[[contact_id]]"
  - "[[dataset_id]]"
  - "[[submission_type_id]]"
columns:
  - "[[date_submitted]]"
  - "[[date_updated]]"
  - "[[notes]]"
connected_tables:
  - "[[tbl_contacts]]"
  - "[[tbl_datasets]]"
  - "[[tbl_dataset_submission_types]]"
date created: Friday, September 19th 2025, 3:37:16 pm
change_it: true
---

Contains records of various submission events related to a dataset, such as initial recording, database entries, and integrations with SEAD.
