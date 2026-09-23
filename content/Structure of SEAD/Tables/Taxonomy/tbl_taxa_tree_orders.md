---
publish: true
permalink: /Structure of SEAD/Tables/Taxonomy/tbl_taxa_tree_orders.md
created: 2026-07-24T09:34:41.475Z
modified: 2026-09-23T05:19:12.875Z
published: 2026-09-23T05:19:12.875Z
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
change_it: true
---

Represents the taxonomic order level within the taxonomic hierarchy.
