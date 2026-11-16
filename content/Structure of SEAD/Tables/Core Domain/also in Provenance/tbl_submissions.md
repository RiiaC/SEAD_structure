---
publish: true
permalink: /Structure of SEAD/Tables/Core Domain/also in Provenance/tbl_submissions.md
created: 2026-11-13T16:47:54.146Z
modified: 2026-11-16T06:25:30.285Z
published: 2026-11-16T06:25:30.285Z
table_name: tbl_submissions
primary_key: "[[submission_id]]"
columns:
  - "[[issue_identifier]]"
  - "[[notes]]"
  - "[[Structure of SEAD/Columns/author|author]]"
  - "[[submission_date]]"
  - "[[submission_identifier]]"
  - "[[upload_date]]"
connected_tables:
foreign_keys:
  - "[[biblio_id]]"
  - "[[submission_state_id]]"
role: fact
required: No
domain:
  - core
  - provenance
---

> [!abstract] Metadata that groups datasets delivered by one data provider.
