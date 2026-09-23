---
publish: true
permalink: /Structure of SEAD/Tables/Sites/tbl_site_preservation_status.md
created: 2026-07-24T09:34:41.300Z
modified: 2026-09-23T05:19:11.035Z
published: 2026-09-23T05:19:11.035Z
table_name: tbl_site_preservation_status
primary_key: "[[site_preservation_status_id]]"
foreign_keys:
  - "[[tbl_locations]]"
columns:
  - "[[Evaluation_date]]"
  - "[[assessment_author_contact_id]]"
  - "[[assessment_type]]"
  - "[[date_updated]]"
  - "[[description]]"
  - "[[preservation_status_or_threat]]"
  - "[[site_id]]"
connected_tables:
  - "[[tbl_sites]]"
change_it: true
---

Contains data on the preservation levels and threats to cultural heritage sites. Each record represents a unique preservation status or threat. This information was added at the request of PAN (Polar Archaeology Network) members to support the evaluation of threats to Arctic cultural heritage.
