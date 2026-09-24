---
publish: true
permalink: /Structure of SEAD/Tables/Dataset/tbl_dataset_masters.md
created: 2026-07-24T09:34:40.950Z
modified: 2026-09-24T05:44:40.546Z
published: 2026-09-24T05:44:40.546Z
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
date created: Friday, September 19th 2025, 3:37:16 pm
---

> [!info] Represents a major grouping identifier for datasets, typically indicating a contributing database, project, user, or laboratory (e.g., BugsCEP, MAL, Lund Dendro Lab).
