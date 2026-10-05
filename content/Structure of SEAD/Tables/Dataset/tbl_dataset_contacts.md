---
publish: true
permalink: /Structure of SEAD/Tables/Dataset/tbl_dataset_contacts.md
created: 2026-07-24T09:34:40.946Z
modified: 2026-10-02T09:16:36.882Z
published: 2026-10-02T09:16:36.882Z
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
---

> [!info] Contains information about one or more contacts related to a dataset, such as data providers or digitalisers.
