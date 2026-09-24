---
publish: true
permalink: /Structure of SEAD/Tables/Ungrouped/tbl_mcr_summary_data.md
created: 2026-07-24T09:34:41.617Z
modified: 2026-09-24T05:44:41.409Z
published: 2026-09-24T05:44:41.409Z
table_name: tbl_mcr_summary_data
primary_key: "[[mcr_summary_data_id]]"
foreign_keys:
  - "[[taxon_id]]"
columns:
  - "[[cog_mid_tmax]]"
  - "[[cog_mid_trange]]"
  - "[[date_updated]]"
  - "[[tmax_hi]]"
  - "[[tmax_lo]]"
  - "[[tmin_hi]]"
  - "[[tmin_lo]]"
  - "[[trange_hi]]"
  - "[[trange_lo]]"
connected_tables:
  - "[[tbl_taxa_tree_master]]"
---

Contains concise summaries detailing the temperature tolerance limits of MCR species.
