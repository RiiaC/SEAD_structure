---
table_name: tbl_isotope_measurements
primary_key: "[[isotope_measurement_id]]"
foreign_keys:
  - "[[isotope_standard_id]]"
  - "[[isotope_type_id]]"
  - "[[method_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_isotope_standards]]"
  - "[[tbl_isotope_types]]"
  - "[[tbl_methods]]"
---

nan
