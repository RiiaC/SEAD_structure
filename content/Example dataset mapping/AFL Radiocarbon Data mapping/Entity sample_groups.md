---
publish: true
permalink: /Example dataset mapping/AFL Radiocarbon Data mapping/Entity sample_groups.md
created: 2026-07-24T09:34:08.013Z
modified: 2026-09-24T05:44:36.937Z
published: 2026-09-24T05:44:36.937Z
Entity_Name: sample_group
Type: Data (Derived)
Public_ID: "[[sample_group_id]]"
Target_Entity: "[[Example dataset mapping/AFL Radiocarbon Data mapping/Entity site]]"
Local_Keys:
  - site
Remote_Keys:
  - system_id
SEAD_table: "[[tbl_sample_groups]]"
status: complete
---

> [!info] SEAD requires all physical samples to be part of a sample group, even if there is only one sample in the group, as it is the sample group that has the connection to a site.
> Therefore this layer is added, as an intermediary layer between the [[Example dataset mapping/AFL Radiocarbon Data mapping/Entity physical_samples]] and [[Example dataset mapping/AFL Radiocarbon Data mapping/Entity site]]

![[images/Entity sample_groups schema.png]]
