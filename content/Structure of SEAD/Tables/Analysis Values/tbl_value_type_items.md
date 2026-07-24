---
table_name: tbl_value_type_items
primary_key: "[[value_type_item_id]]"
foreign_keys:
  - "[[value_type_id]]"
columns:
  - "[[source/docs/plugins/Description]]"
  - "[[name]]"
connected_tables:
  - "[[tbl_value_types]]"
---

Defines individual category values if value type is categorical
