---
publish: true
permalink: /Structure of SEAD/Tables/Analysis Domain/tbl_analysis_taxon_counts.md
created: 2026-07-24T09:34:40.896Z
modified: 2026-11-13T16:36:20.046Z
published: 2026-11-13T16:36:20.046Z
table_name: tbl_analysis_taxon_counts
primary_key: "[[analysis_taxon_count_id]]"
columns:
  - "[[value]]"
connected_tables:
  - "[[tbl_analysis_values]]"
  - "[[tbl_taxa_tree_master]]"
foreign_keys:
  - "[[analysis_value_id]]"
  - "[[taxon_id]]"
required: No
role: fact
domain:
  - analysis
  - taxonomy
---

> [!abstract] Taxon-specific count attached to an analysis value.
> Storage for analysis values that represents a taxon counts.
