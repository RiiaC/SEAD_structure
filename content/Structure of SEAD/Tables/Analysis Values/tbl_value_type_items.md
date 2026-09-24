---
table_name: tbl_value_type_items
primary_key: "[[value_type_item_id]]"
foreign_keys:
  - "[[value_type_id]]"
columns:
  - "[[description]]"
  - "[[name]]"
connected_tables:
  - "[[tbl_value_types]]"
publish: true
---

Defines individual category values if value type is categorical
