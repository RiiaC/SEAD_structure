---
publish: true
permalink: /Structure of SEAD/Tables/Ungrouped/core/tbl_physical_samples.md
created: 2026-07-24T09:34:41.325Z
modified: 2026-11-16T12:46:46.233Z
published: 2026-11-16T12:46:46.233Z
table_name: tbl_physical_samples
primary_key: "[[physical_sample_id]]"
columns:
  - "[[date_sampled]]"
  - "[[date_updated]]"
  - "[[sample_name]]"
foreign_keys:
  - "[[alt_ref_type_id]]"
  - "[[sample_group_id]]"
  - "[[sample_type_id]]"
connected_tables:
  - "[[tbl_alt_ref_types]]"
  - "[[tbl_sample_groups]]"
  - "[[tbl_sample_types]]"
required: Yes
role: fact
domain:
  - core
---

> [!abstract] Core analytical specimen represented in SEAD as a physical sample.
> Records information about physical samples collected from specific sites. Each sample is characterized by its location within the site, its physical properties measured in specific units (e.g., liters, kilograms), and its context within a sample set. Additionally, samples may have descriptive information, notes, and external identifiers linked to other systems.
