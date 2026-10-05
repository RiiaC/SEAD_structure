---
publish: true
permalink: /Structure of SEAD/Tables/Dimensions/tbl_analysis_entity_dimensions.md
created: 2026-07-24T09:34:41.064Z
modified: 2026-10-02T09:16:36.934Z
published: 2026-10-02T09:16:36.934Z
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
---

Contains information about the physical dimensions of samples used for analysis, including both analyzed samples and non-analyzed residues.
