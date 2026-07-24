---
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
---

Contains records of various submission events related to a dataset, such as initial recording, database entries, and integrations with SEAD.
