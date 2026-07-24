---
table_name: tbl_analysis_notes
primary_key: "[[analysis_note_id]]"
foreign_keys:
  - "[[analysis_value_id]]"
columns:
  - "[[value]]"
connected_tables:
  - "[[tbl_analysis_values]]"
---

Storage for notes associated to an analysis value.
