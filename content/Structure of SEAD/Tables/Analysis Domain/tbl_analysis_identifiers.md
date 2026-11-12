---
publish: true
permalink: /Structure of SEAD/Tables/Analysis Domain/tbl_analysis_identifiers.md
created: 2026-07-24T09:34:40.868Z
modified: 2026-11-12T06:09:57.824Z
published: 2026-11-12T06:09:57.824Z
table_name: tbl_analysis_identifiers
primary_key: "[[analysis_identifier_id]]"
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

> [!info] Identifier string attached to an analysis value.
> Storage for identifiers associated to analysis values, or analysis value that represents an identifier.
