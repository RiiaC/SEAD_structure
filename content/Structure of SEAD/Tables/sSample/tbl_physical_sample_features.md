---
table_name: tbl_physical_sample_features
primary_key: "[[physical_sample_feature_id]]"
foreign_keys:
  - "[[feature_id]]"
  - "[[physical_sample_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_features]]"
  - "[[tbl_physical_samples]]"
---

Establishes a many-to-many relationship between samples and specific features, allowing a feature to be related to multiple samples and a sample to be linked to multiple features. This supports scenarios where samples originate from nested feature groups or features with multiple identifiers.
