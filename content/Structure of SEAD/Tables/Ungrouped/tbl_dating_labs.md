---
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
