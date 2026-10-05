---
publish: true
permalink: /Structure of SEAD/Tables/Geochronology/tbl_chronologies.md
created: 2026-07-24T09:34:40.846Z
modified: 2026-10-02T09:16:36.974Z
published: 2026-10-02T09:16:36.974Z
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
---

> [!info] Represents a collection of dated samples grouped for specific purposes, such as assigning a unified age range to samples in a master dataset or developing an age-depth model for a lake. These chronologies may also be used to integrate with external services that limit the scope of dating evidence, such as GBIF or SBDI.
