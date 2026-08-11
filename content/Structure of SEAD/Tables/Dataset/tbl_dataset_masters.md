---
table_name: tbl_dataset_masters
primary_key: "[[master_set_id]]"
foreign_keys:
  - "[[biblio_id]]"
  - "[[contact_id]]"
columns:
  - "[[date_updated]]"
  - "[[master_name]]"
  - "[[master_notes]]"
  - "[[master_set_uuid]]"
  - "[[url]]"
connected_tables:
  - "[[tbl_biblio]]"
  - "[[tbl_contacts]]"
date created: Friday, September 19th 2025, 3:37:16 pm
publish: true
---
> [!info] Represents a major grouping identifier for datasets, typically indicating a contributing database, project, user, or laboratory (e.g., BugsCEP, MAL, Lund Dendro Lab).
