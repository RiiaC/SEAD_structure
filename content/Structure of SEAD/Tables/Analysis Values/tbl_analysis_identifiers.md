---
table_name: tbl_analysis_identifiers
primary_key: "[[analysis_identifier_id]]"
foreign_keys:
  - "[[analysis_value_id]]"
columns:
  - "[[value]]"
connected_tables:
  - "[[tbl_analysis_values]]"
---

Storage for identifiers associated to analysis values, or analysis value that represents an identifier.
