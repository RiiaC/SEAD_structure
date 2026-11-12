---
publish: true
permalink: /Structure of SEAD/Tables/Analysis Domain/tbl_analysis_notes.md
created: 2026-07-24T09:34:40.876Z
modified: 2026-11-12T06:11:40.160Z
published: 2026-11-12T06:11:40.160Z
table_name: tbl_analysis_notes
primary_key: "[[analysis_note_id]]"
columns:
  - "[[value]]"
connected_tables:
  - "[[tbl_analysis_values]]"
foreign_keys:
  - "[[analysis_value_id]]"
required: No
role: fact
domain:
  - analysis
---

> [!info] Free-text note attached to an analysis value.
> Storage for notes associated to an analysis value.
