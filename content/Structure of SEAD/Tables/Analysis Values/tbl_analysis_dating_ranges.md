---
table_name: tbl_analysis_dating_ranges
primary_key: "[[analysis_dating_range_id]]"
foreign_keys:
  - "[[age_type_id]]"
  - "[[analysis_value_id]]"
  - "[[dating_uncertainty_id]]"
  - "[[high_qualifier]]"
  - "[[low_qualifier]]"
  - "[[season_id]]"
columns:
  - "[[high_is_uncertain]]"
  - "[[high_value]]"
  - "[[is_variant]]"
  - "[[low_is_uncertain]]"
  - "[[low_value]]"
connected_tables:
  - "[[tbl_age_types]]"
  - "[[tbl_analysis_values]]"
  - "[[tbl_dating_uncertainty]]"
  - "[[tbl_value_qualifier_symbols]]"
  - "[[tbl_seasons]]"
---

Storage for analysis values that represents a dating range.
