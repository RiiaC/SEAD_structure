---
publish: true
permalink: /Structure of SEAD/Tables/Core Domain/Sample/tbl_physical_sample_features.md
created: 2026-07-24T09:34:41.330Z
modified: 2026-11-13T09:58:00.033Z
published: 2026-11-13T09:58:00.033Z
table_name: tbl_physical_sample_features
primary_key: "[[physical_sample_feature_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_features]]"
  - "[[tbl_physical_samples]]"
foreign_keys:
  - "[[feature_id]]"
  - "[[physical_sample_id]]"
---

Establishes a many-to-many relationship between samples and specific features, allowing a feature to be related to multiple samples and a sample to be linked to multiple features. This supports scenarios where samples originate from nested feature groups or features with multiple identifiers.
