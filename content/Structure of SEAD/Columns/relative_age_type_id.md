---
column_name: relative_age_type_id
data_type: integer
connected_tables:
  - "[[tbl_chronologies]]"
  - "[[tbl_relative_age_types]]"
  - "[[tbl_relative_ages]]"
publish: true
---

This was previously constrained by the obsolete tbl\_age\_types table. Now, it serves as a non-binding reference to relative\_age\_types, although not fully implemented. Relevant notes should document year types and construction methods for the chronology.
