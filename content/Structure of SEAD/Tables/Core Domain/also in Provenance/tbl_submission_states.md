---
publish: true
permalink: /Structure of SEAD/Tables/Core Domain/also in Provenance/tbl_submission_states.md
created: 2026-11-16T06:26:46.885Z
modified: 2026-11-16T14:14:17.129Z
published: 2026-11-16T14:14:17.129Z
table_name: tbl_submission_states
primary_key: "[[submission_state_id]]"
columns:
  - "[[note]]"
  - "[[submission_state]]"
connected_tables:
  - "[[tbl_submissions]]"
required: No
role: classifier
domain:
  - core
  - provenance
---

> [!abstract] Defines the lifecycle states available to submissions.

# proposed list of submission states

as of 2026-11-16

|[[submission_state_id]]|[[submission_state]]| [[note]]|
|---|---|---|
|1|'Pending'|'Submission is pending review'|
|2|'Approved'|'Submission has been approved'|
|3|'Rejected'|'Submission has been rejected'|
|4|'Pulled'|'Submission has been pulled'|
|5|'Future'|'Submission is scheduled for future upload|
