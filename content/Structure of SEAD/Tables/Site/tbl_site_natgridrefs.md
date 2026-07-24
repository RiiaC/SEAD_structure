---
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
