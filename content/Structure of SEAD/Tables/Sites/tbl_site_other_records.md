---
publish: true
permalink: /Structure of SEAD/Tables/Sites/tbl_site_other_records.md
created: 2026-07-24T09:34:41.296Z
modified: 2026-09-23T05:19:11.055Z
published: 2026-09-23T05:19:11.055Z
table_name: tbl_site_other_records
primary_key: "[[site_other_records_id]]"
foreign_keys:
  - "[[biblio_id]]"
  - "[[record_type_id]]"
  - "[[site_id]]"
  - "[[tbl_locations]]"
columns:
  - "[[date_updated]]"
  - "[[description]]"
  - "[[site_other_records_uuid]]"
connected_tables:
  - "[[tbl_biblio]]"
  - "[[tbl_record_types]]"
  - "[[tbl_sites]]"
change_it: true
---

Contains information about data related to specific sites that is not currently stored in SEAD. Each record corresponds to a distinct proxy type, even if multiple proxies are linked to the same publication. Note that some of these datasets might be integrated into SEAD in the future. Requests for data submission can be directed to the SEAD project team.
