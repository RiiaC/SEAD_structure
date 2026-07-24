---
table_name: tbl_value_classes
primary_key: "[[value_class_id]]"
foreign_keys:
  - "[[method_id]]"
  - "[[parent_id]]"
  - "[[value_type_id]]"
columns:
  - "[[source/docs/plugins/Description]]"
  - "[[name]]"
  - "[[value_class_uuid]]"
connected_tables:
  - "[[tbl_methods]]"
  - "[[tbl_value_classes]]"
  - "[[tbl_value_types]]"
---

Specifies a value class describing e.g. a data column
