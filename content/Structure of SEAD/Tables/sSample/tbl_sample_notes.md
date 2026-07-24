---
table_name: tbl_sample_notes
primary_key: "[[sample_note_id]]"
foreign_keys:
  - "[[physical_sample_id]]"
columns:
  - "[[date_updated]]"
  - "[[note]]"
  - "[[note_type]]"
connected_tables:
  - "[[tbl_physical_samples]]"
---

Contains miscellaneous notes related to samples that do not belong in other tables, such as 'stored in a cellar until processing in 2020'.
