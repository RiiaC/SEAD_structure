---
table_name: tbl_site_other_records
primary_key: "[[site_other_records_id]]"
foreign_keys:
  - "[[biblio_id]]"
  - "[[record_type_id]]"
  - "[[site_id]]"
  - "[[tbl_locations]]"
columns:
  - "[[date_updated]]"
  - "[[source/docs/plugins/Description]]"
  - "[[site_other_records_uuid]]"
connected_tables:
  - "[[tbl_biblio]]"
  - "[[tbl_record_types]]"
  - "[[tbl_sites]]"
---

Contains information about data related to specific sites that is not currently stored in SEAD. Each record corresponds to a distinct proxy type, even if multiple proxies are linked to the same publication. Note that some of these datasets might be integrated into SEAD in the future. Requests for data submission can be directed to the SEAD project team.
