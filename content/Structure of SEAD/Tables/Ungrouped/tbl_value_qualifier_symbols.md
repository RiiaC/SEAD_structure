---
table_name: tbl_value_qualifier_symbols
primary_key: "[[qualifier_symbol_id]]"
foreign_keys:
  - "[[cardinal_qualifier_id]]"
columns:
  - "[[qualifier_uuid]]"
  - "[[symbol]]"
connected_tables:
  - "[[tbl_value_qualifiers]]"
---

Specifies alternative symbols for value qualifiers
