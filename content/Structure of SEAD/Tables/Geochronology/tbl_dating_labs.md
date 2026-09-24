---
publish: true
permalink: /Structure of SEAD/Tables/Geochronology/tbl_dating_labs.md
created: 2026-07-24T09:34:41.540Z
modified: 2026-09-24T05:44:40.679Z
published: 2026-09-24T05:44:40.679Z
table_name: tbl_dating_labs
primary_key: "[[dating_lab_id]]"
foreign_keys:
  - "[[contact_id]]"
columns:
  - "[[country_id]]"
  - "[[date_updated]]"
  - "[[international_lab_id]]"
  - "[[lab_name]]"
connected_tables:
  - "[[tbl_contacts]]"
---

Contains identifiers and names of radiocarbon laboratories sourced from radiocarbon.org/laboratories. Ensures transparency and traceability in radiocarbon and other radiometric dating records.
