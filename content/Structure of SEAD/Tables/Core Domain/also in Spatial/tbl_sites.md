---
publish: true
permalink: /Structure of SEAD/Tables/Core Domain/also in Spatial/tbl_sites.md
created: 2026-07-24T09:34:41.278Z
modified: 2026-11-16T08:49:18.125Z
published: 2026-11-16T08:49:18.125Z
table_name: tbl_sites
primary_key: "[[site_id]]"
columns:
  - "[[altitude]]"
  - "[[latitude_dd]]"
  - "[[longitude_dd]]"
  - "[[national_site_identifier]]"
  - "[[site_description]]"
  - "[[site_location_accuracy]]"
  - "[[site_name]]"
  - "[[site_uuid]]"
connected_tables:
  - "[[tbl_site_preservation_status]]"
foreign_keys:
  - "[[site_preservation_status_id]]"
url: https://humlab-sead.github.io/sead-schema/tables/tbl_sites.html
required: Yes
role: lookup
domain:
  - core
  - spatial
---

> [!abstract] Archaeological site anchored to a location.
> Records detailed information about each excavation or sampling location i.e. a defined location where samples have been collected through excavation.
