---
publish: true
permalink: /Structure of SEAD/Tables/Excavation Domain/tbl_feature_properties.md
created: 2026-11-16T13:53:02.636Z
modified: 2026-11-16T13:57:49.214Z
published: 2026-11-16T13:57:49.214Z
table_name: tbl_feature_properties
primary_key: "[[feature_property_id]]"
columns:
  - "[[property_value]]"
foreign_keys:
  - "[[feature_id]]"
  - "[[property_type_id]]"
connected_tables:
  - "[[tbl_features]]"
  - "[[tbl_property_type]]"
required: No
role: fact
domain:
  - excavation
---

> [!abstract] Property/value observation attached to an archaeological feature.
> Stores property values assigned to features.
