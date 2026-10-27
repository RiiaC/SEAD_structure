---
publish: true
permalink: /Structure of SEAD/Columns/lab_number.md
created: 2026-07-24T09:34:39.862Z
modified: 2026-09-24T05:44:39.245Z
published: 2026-09-24T05:44:39.245Z
column_name: lab_number
data_type: character varying
connected_tables:
  - "[[tbl_geochronology]]"
---

Identifier assigned by the laboratory for the sample.

> [!note] This column is specifically for radiocarbon laboratory lab numbers
> Use this for samples that have undergone radiocarbon dating. For lab numbers associated with other sorts of laboratory analysis, use the he [alt\_ref](app://obsidian.md/alt_ref) column of [tbl\_sample\_alt\_refs](app://obsidian.md/tbl_sample_alt_refs), where [alt\_ref\_type](app://obsidian.md/alt_ref_type) = 3 = Lab Number.
