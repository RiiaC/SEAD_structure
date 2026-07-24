---
table_name: tbl_analysis_entity_prep_methods
primary_key: "[[analysis_entity_prep_method_id]]"
foreign_keys:
  - "[[analysis_entity_id]]"
  - "[[method_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_analysis_entities]]"
  - "[[tbl_methods]]"
---

Links analysis entities with their respective preparation methods.
