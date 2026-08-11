---
table_name: tbl_site_references
primary_key: "[[site_reference_id]]"
foreign_keys:
  - "[[biblio_id]]"
  - "[[site_id]]"
  - "[[tbl_locations]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_biblio]]"
  - "[[tbl_sites]]"
date created: Friday, September 19th 2025, 3:37:16 pm
publish: true
---

Catalogs publications that describe or mention sites. Publications related to specific sample groups, physical samples, or datasets are documented at their respective hierarchical levels.
