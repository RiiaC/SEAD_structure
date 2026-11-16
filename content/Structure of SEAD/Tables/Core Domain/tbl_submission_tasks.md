---
publish: true
permalink: /Structure of SEAD/Tables/Core Domain/tbl_submission_tasks.md
created: 2026-11-16T07:44:28.497Z
modified: 2026-11-16T07:58:23.329Z
published: 2026-11-16T07:58:23.329Z
table_name: tbl_submission_tasks
primary_key: "[[submission_task_id]]"
columns:
  - "[[notes]]"
  - event_date
connected_tables:
foreign_keys:
  - "[[biblio_id]]"
  - "[[contact_id]]"
  - "[[event_date]]"
  - "[[submission_id]]"
  - "[[submission_task_type_id]]"
role: fact
required: No
domain:
  - core
  - provenance
---

> [!abstract] Records submission tasks and the contacts responsible for them.
