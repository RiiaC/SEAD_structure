---
table_name: tbl_value_types
primary_key: "[[value_type_id]]"
foreign_keys:
  - "[[data_type_id]]"
  - "[[unit_id]]"
columns:
  - "[[base_type]]"
  - "[[source/docs/plugins/Description]]"
  - "[[name]]"
  - "[[precision]]"
  - "[[value_type_uuid]]"
connected_tables:
  - "[[tbl_data_types]]"
  - "[[tbl_units]]"
---

Specifies actual type of values belonging to a value class
