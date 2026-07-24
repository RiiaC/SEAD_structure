---
table_name: tbl_physical_samples
primary_key: "[[physical_sample_id]]"
foreign_keys:
  - "[[alt_ref_type_id]]"
  - "[[sample_group_id]]"
  - "[[sample_type_id]]"
columns:
  - "[[date_sampled]]"
  - "[[date_updated]]"
  - "[[sample_name]]"
connected_tables:
  - "[[tbl_alt_ref_types]]"
  - "[[tbl_sample_groups]]"
  - "[[tbl_sample_types]]"
date created: Friday, September 19th 2025, 3:37:16 pm
---

Records information about physical samples collected from specific sites. Each sample is characterized by its location within the site, its physical properties measured in specific units (e.g., liters, kilograms), and its context within a sample set. Additionally, samples may have descriptive information, notes, and external identifiers linked to other systems.
