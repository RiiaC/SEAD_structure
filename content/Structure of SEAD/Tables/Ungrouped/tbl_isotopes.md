---
table_name: tbl_isotopes
primary_key: "[[isotope_id]]"
foreign_keys:
  - "[[analysis_entity_id]]"
  - "[[isotope_measurement_id]]"
  - "[[isotope_standard_id]]"
  - "[[isotope_value_specifier_id]]"
  - "[[unit_id]]"
columns:
  - "[[date_updated]]"
  - "[[measurement_value]]"
connected_tables:
  - "[[tbl_analysis_entities]]"
  - "[[tbl_isotope_measurements]]"
  - "[[tbl_isotope_standards]]"
  - "[[tbl_isotope_value_specifiers]]"
  - "[[tbl_units]]"
---

nan
