---
table_name: tbl_analysis_entity_ages
primary_key: "[[analysis_entity_age_id]]"
foreign_keys:
  - "[[analysis_entity_id]]"
  - "[[chronology_id]]"
columns:
  - "[[age]]"
  - "[[age_older]]"
  - "[[age_range]]"
  - "[[age_younger]]"
  - "[[date_updated]]"
  - "[[dating_specifier]]"
connected_tables:
  - "[[tbl_analysis_entities]]"
  - "[[tbl_chronologies]]"
publish: true
---

> [!info] Represents a virtual entity that defines a single proxy within a specific physical sample, acting as a statistical sample. A physical sample can contain multiple analysis entities, each linking various proxies. This structure facilitates the precise recording of specific species used in methods like radiocarbon dating.
