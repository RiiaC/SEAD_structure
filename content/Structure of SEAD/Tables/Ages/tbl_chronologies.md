---
table_name: tbl_chronologies
primary_key: "[[chronology_id]]"
foreign_keys:
  - "[[contact_id]]"
columns:
  - "[[age_model]]"
  - "[[chronology_name]]"
  - "[[date_prepared]]"
  - "[[date_updated]]"
  - "[[notes]]"
  - "[[relative_age_type_id]]"
connected_tables:
  - "[[tbl_contacts]]"
date created: Friday, September 19th 2025, 3:37:16 pm
---
> [!info] Represents a collection of dated samples grouped for specific purposes, such as assigning a unified age range to samples in a master dataset or developing an age-depth model for a lake. These chronologies may also be used to integrate with external services that limit the scope of dating evidence, such as GBIF or SBDI.
