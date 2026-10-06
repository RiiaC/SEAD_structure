---
publish: true
permalink: /Structure of SEAD/Tables/Taxonomy/tbl_taxa_common_names.md
created: 2026-07-24T09:34:41.431Z
modified: 2026-10-06T09:26:28.721Z
published: 2026-10-06T09:26:28.721Z
Entity_Name:
Type:
Public_ID:
table_name: tbl_taxa_common_names
primary_key: "[[taxon_common_name_id]]"
columns:
  - "[[common_name]]"
  - "[[date_updated]]"
connected_tables:
  - "[[tbl_languages]]"
  - "[[tbl_taxa_tree_master]]"
Target_Entity:
Local_Keys:
Remote_Keys:
SEAD_table:
status:
foreign_keys:
  - "[[language_id]]"
  - "[[taxon_id]]"
---

Stores vernacular or common names of organisms, such as 'bluebottle'.
