---
publish: true
permalink: /Structure of SEAD/Tables/Dating Domain/tbl_dating_labs.md
created: 2026-07-24T09:34:41.540Z
modified: 2026-11-16T13:19:10.548Z
published: 2026-11-16T13:19:10.548Z
table_name: tbl_dating_labs
primary_key: "[[dating_lab_id]]"
columns:
  - "[[country_id]]"
  - "[[date_updated]]"
  - "[[international_lab_id]]"
  - "[[lab_name]]"
foreign_keys:
  - "[[contact_id]]"
connected_tables:
  - "[[tbl_contacts]]"
required: No
role: lookup
domain:
  - dating
---

> [!abstract] Laboratory metadata for dated samples and geochronology results.
> Contains identifiers and names of radiocarbon laboratories sourced from radiocarbon.org/laboratories. Ensures transparency and traceability in radiocarbon and other radiometric dating records.
