---
table_name: tbl_taxa_tree_orders
primary_key: "[[order_id]]"
foreign_keys:
  - "[[record_type_id]]"
columns:
  - "[[date_updated]]"
  - "[[order_name]]"
  - "[[sort_order]]"
connected_tables:
  - "[[tbl_record_types]]"
---

Represents the taxonomic order level within the taxonomic hierarchy.
