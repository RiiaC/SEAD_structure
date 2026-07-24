---
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
---

Contains information about the physical dimensions of samples used for analysis, including both analyzed samples and non-analyzed residues.
