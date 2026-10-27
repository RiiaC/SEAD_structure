---
publish: true
permalink: /Structure of SEAD/Tables/Dataset/tbl_data_providers.md
created: 2026-10-27T14:00:49.180Z
modified: 2026-10-27T14:06:17.173Z
published: 2026-10-27T14:06:17.173Z
table_name: tbl_dataset_submissions
primary_key: "[[data_provider_id]]"
columns:
  - "[[biblio_id]]"
  - "[[contact_id]]"
  - "[[data_provider_code]]"
  - "[[data_provider_name]]"
  - "[[data_provider_uuid]]"
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

A new table as of 2026, as we now require information on the individual or group providing the data
