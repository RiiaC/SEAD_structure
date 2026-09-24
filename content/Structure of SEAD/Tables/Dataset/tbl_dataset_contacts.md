---
publish: true
permalink: /Structure of SEAD/Tables/Dataset/tbl_dataset_contacts.md
created: 2026-07-24T09:34:40.946Z
modified: 2026-09-24T05:44:40.539Z
published: 2026-09-24T05:44:40.539Z
table_name: tbl_dataset_contacts
primary_key: "[[dataset_contact_id]]"
foreign_keys:
  - "[[contact_id]]"
  - "[[contact_type_id]]"
  - "[[dataset_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_contacts]]"
  - "[[tbl_contact_types]]"
  - "[[tbl_datasets]]"
date created: Friday, September 19th 2025, 3:37:16 pm
---

> [!info] Contains information about one or more contacts related to a dataset, such as data providers or digitalisers.
