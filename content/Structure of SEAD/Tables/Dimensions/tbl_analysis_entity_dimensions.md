---
publish: true
permalink: /Structure of SEAD/Tables/Dimensions/tbl_analysis_entity_dimensions.md
created: 2026-07-24T09:34:41.064Z
modified: 2026-09-23T05:19:10.180Z
published: 2026-09-23T05:19:10.180Z
table_name: tbl_analysis_entity_dimensions
primary_key: "[[analysis_entity_dimension_id]]"
foreign_keys:
  - "[[analysis_entity_id]]"
  - "[[dimension_id]]"
columns:
  - "[[date_updated]]"
  - "[[dimension_value]]"
connected_tables:
  - "[[tbl_analysis_entities]]"
  - "[[tbl_dimensions]]"
date created: Friday, September 19th 2025, 3:37:16 pm
change_it: true
---

Contains information about the physical dimensions of samples used for analysis, including both analyzed samples and non-analyzed residues.
