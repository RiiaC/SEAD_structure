---
publish: true
permalink: /Structure of SEAD/Tables/Sites/tbl_site_natgridrefs.md
created: 2026-07-24T09:34:41.290Z
modified: 2026-09-24T05:44:41.096Z
published: 2026-09-24T05:44:41.096Z
table_name: tbl_site_natgridrefs
primary_key: "[[site_natgridref_id]]"
foreign_keys:
  - "[[method_id]]"
  - "[[site_id]]"
  - "[[tbl_locations]]"
columns:
  - "[[date_updated]]"
  - "[[natgridref]]"
connected_tables:
  - "[[tbl_methods]]"
  - "[[tbl_sites]]"
---

Contains site coordinates using various national grid systems, such as the UK Ordnance Survey National Grid and Swedish SWEREF99. Each site may have coordinates in multiple grid systems (e.g., Swedish RT90 and SWEREF99TM).

Note that this table had not yet been used as of July 2026.
