---
publish: true
permalink: /Structure of SEAD/Tables/Analysis Domain/tbl_value_type_items.md
created: 2026-07-24T09:34:40.919Z
modified: 2026-11-13T16:33:49.310Z
published: 2026-11-13T16:33:49.310Z
table_name: tbl_value_type_items
primary_key: "[[value_type_item_id]]"
columns:
  - "[[description]]"
  - "[[name]]"
connected_tables:
  - "[[tbl_value_types]]"
foreign_keys:
  - "[[value_type_id]]"
required: No
role: classifier
domain:
  - analysis
---

> [!Abstract]  Category value attached to a categorical value type.
> Defines individual category values if value type is categorical

As of 2026-11-12 this table has only been used for dendrochronology data where they have recorded different specific types dendro data that fall into the broader categories in the [[tbl_value_types]] list.
