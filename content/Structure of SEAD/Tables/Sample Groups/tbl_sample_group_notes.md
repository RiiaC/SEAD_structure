---
table_name: tbl_sample_group_notes
primary_key: "[[sample_group_note_id]]"
foreign_keys:
  - "[[sample_group_id]]"
columns:
  - "[[date_updated]]"
  - "[[note]]"
connected_tables:
  - "[[tbl_sample_groups]]"
---

Contains notes pertaining to groups of samples.
