---
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
