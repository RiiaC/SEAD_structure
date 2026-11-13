---
publish: true
permalink: /Structure of SEAD/Tables/Analysis Domain/tbl_analysis_notes.md
created: 2026-07-24T09:34:40.876Z
modified: 2026-11-13T16:37:41.150Z
published: 2026-11-13T16:37:41.150Z
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

> [!abstract] Free-text note attached to an analysis value.
> Storage for notes associated to an analysis value.
