---
publish: true
permalink: /Structure of SEAD/Tables/Sites/tbl_site_references.md
created: 2026-07-24T09:34:41.311Z
modified: 2026-10-02T09:16:37.293Z
published: 2026-10-02T09:16:37.293Z
table_name: tbl_site_references
primary_key: "[[site_reference_id]]"
columns:
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_biblio]]"
  - "[[tbl_sites]]"
foreign_keys:
  - "[[biblio_id]]"
  - "[[site_id]]"
  - "[[tbl_locations]]"
---

Catalogs publications that describe or mention sites. Publications related to specific sample groups, physical samples, or datasets are documented at their respective hierarchical levels.
