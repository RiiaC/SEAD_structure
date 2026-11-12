---
publish: true
permalink: /Structure of SEAD/Tables/Dimensions/tbl_analysis_value_dimensions.md
created: 2026-07-24T09:34:40.905Z
modified: 2026-11-12T06:17:36.544Z
published: 2026-11-12T06:17:36.544Z
table_name: tbl_analysis_value_dimensions
primary_key: "[[analysis_value_dimension_id]]"
columns:
  - "[[value]]"
connected_tables:
  - "[[tbl_analysis_values]]"
  - "[[tbl_dimensions]]"
foreign_keys:
  - "[[analysis_value_id]]"
  - "[[dimension_id]]"
required: No
role: fact
domain:
  - analysis
---

> [!info]  Dimension measurement attached directly to an analysis value.
> Storage for dimension of analysis value.
