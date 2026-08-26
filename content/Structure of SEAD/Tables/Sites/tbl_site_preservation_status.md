---
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
publish: true
---

Contains data on the preservation levels and threats to cultural heritage sites. Each record represents a unique preservation status or threat. This information was added at the request of PAN (Polar Archaeology Network) members to support the evaluation of threats to Arctic cultural heritage.
