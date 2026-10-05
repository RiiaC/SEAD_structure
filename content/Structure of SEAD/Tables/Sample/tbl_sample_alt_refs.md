---
publish: true
permalink: /Structure of SEAD/Tables/Sample/tbl_sample_alt_refs.md
created: 2026-07-24T09:34:41.331Z
modified: 2026-10-02T09:16:37.165Z
published: 2026-10-02T09:16:37.165Z
table_name: "[[tbl_sample_alt_refs]]"
primary_key: "[[sample_alt_ref_id]]"
columns:
  - "[[alt_ref]]"
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_alt_ref_types]]"
  - "[[tbl_physical_samples]]"
foreign_keys:
  - "[[alt_ref_type_id]]"
  - "[[physical_sample_id]]"
---

Contains various reference names for physical samples, such as laboratory or field numbers.

> [!warning]  Raidocarbon dating lab numbers do not go in this table
> They belong in [[tbl_geochronology]]
