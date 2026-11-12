---
publish: true
permalink: /Structure of SEAD/Tables/Analysis Domain/tbl_analysis_categorical_values.md
created: 2026-07-24T09:34:40.860Z
modified: 2026-11-12T06:06:56.505Z
published: 2026-11-12T06:06:56.505Z
table_name: tbl_analysis_categorical_values
primary_key: "[[analysis_categorical_value_id]]"
columns:
  - "[[is_variant]]"
  - "[[value]]"
connected_tables:
  - "[[tbl_analysis_values]]"
  - "[[tbl_value_type_items]]"
foreign_keys:
  - "[[analysis_value_id]]"
  - "[[value_type_item_id]]"
required: No
role: fact
domain:
  - analysis
---

> [!info] Categorical analysis result linked to a controlled value-type item.
> Storage for analysis values that represents a categorical value.
