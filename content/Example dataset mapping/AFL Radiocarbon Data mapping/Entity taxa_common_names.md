---
publish: true
permalink: /Example dataset mapping/AFL Radiocarbon Data mapping/Entity taxa_common_names.md
created: 2026-07-24T09:34:08.035Z
modified: 2026-09-24T05:44:36.942Z
published: 2026-09-24T05:44:36.942Z
Entity_Name: taxa_common_names
Type: Fixed Values
Public_ID: "[[taxon_common_name_id]]"
Target_Entity: "[[Example dataset mapping/AFL Radiocarbon Data mapping/Entity taxa_tree_master]]"
Local_Keys:
  - "[[taxon_id]]"
Remote_Keys: system_id
status: complete
---

Since this is fixed values, I just created these extra columns, using an internal to this dataset holding value of 1 for the taxon\_id

| New Column Name | Source Column |
| --------------- | ------------- |
| common\_name     | harp seal     |
| taxon\_id        | 1             |

![[images/Entity taxa_common_names schema.png]]
