---
Entity_Name: taxa_common_names
Type: Fixed Values
Public_ID: "[[taxon_common_name_id]]"
Target_Entity: "[[content/Example dataset mapping/AFL Radiocarbon Data mapping/Entity taxa_tree_master]]"
Local_Keys:
  - "[[taxon_id]]"
Remote_Keys: system_id
status: complete
---
Since this is fixed values, I just created these extra columns, using an internal to this dataset holding value of 1 for the taxon_id

| New Column Name | Source Column |
| --------------- | ------------- |
| common_name     | harp seal     |
| taxon_id        | 1             |

![[Entity taxa_common_names schema.png]]