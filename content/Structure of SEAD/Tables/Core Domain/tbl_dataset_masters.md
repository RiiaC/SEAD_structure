---
publish: true
permalink: /Structure of SEAD/Tables/Core Domain/tbl_dataset_masters.md
created: 2026-07-24T09:34:40.950Z
modified: 2026-11-13T16:25:03.612Z
published: 2026-11-13T16:25:03.612Z
table_name: tbl_dataset_masters
primary_key: "[[master_set_id]]"
columns:
  - "[[date_updated]]"
  - "[[master_name]]"
  - "[[master_notes]]"
  - "[[master_set_uuid]]"
  - "[[url]]"
connected_tables:
  - "[[tbl_biblio]]"
  - "[[tbl_contacts]]"
foreign_keys:
  - "[[biblio_id]]"
  - "[[contact_id]]"
required: Yes
role: lookup
domain:
  - contacts
  - core
  - provenance
---

> [!info] Master dataset grouping referenced by one or more datasets.
> Represents a major grouping identifier for datasets, typically indicating a contributing database, project, user, or laboratory (e.g., BugsCEP, MAL, Lund Dendro Lab).
