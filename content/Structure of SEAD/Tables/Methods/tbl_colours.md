---
table_name: tbl_colours
primary_key: "[[colour_id]]"
foreign_keys:
  - "[[method_id]]"
columns:
  - "[[colour_name]]"
  - "[[date_updated]]"
  - "[[rgb]]"
connected_tables:
  - "[[tbl_methods]]"
---

Contains the names and definitions of colours as classified by specific methods or colour spaces, such as Munsell or 2.5YR.
