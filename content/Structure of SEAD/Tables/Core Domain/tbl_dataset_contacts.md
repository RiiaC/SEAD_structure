---
publish: true
permalink: /Structure of SEAD/Tables/Core Domain/tbl_dataset_contacts.md
created: 2026-07-24T09:34:40.946Z
modified: 2026-11-13T16:33:15.795Z
published: 2026-11-13T16:33:15.795Z
table_name: tbl_dataset_contacts
primary_key: "[[dataset_contact_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_contact_types]]"
  - "[[tbl_contacts]]"
  - "[[tbl_datasets]]"
foreign_keys:
  - "[[contact_id]]"
  - "[[contact_type_id]]"
  - "[[dataset_id]]"
required: No
role: bridge
domain:
  - contacts
  - provenance
---

> [!abstract] Many-to-many bridge connecting datasets, contacts, and contact roles.
