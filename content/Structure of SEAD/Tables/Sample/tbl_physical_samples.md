---
publish: true
permalink: /Structure of SEAD/Tables/Sample/tbl_physical_samples.md
created: 2026-07-24T09:34:41.325Z
modified: 2026-10-02T09:16:37.141Z
published: 2026-10-02T09:16:37.141Z
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
---

Records information about physical samples collected from specific sites. Each sample is characterized by its location within the site, its physical properties measured in specific units (e.g., liters, kilograms), and its context within a sample set. Additionally, samples may have descriptive information, notes, and external identifiers linked to other systems.
