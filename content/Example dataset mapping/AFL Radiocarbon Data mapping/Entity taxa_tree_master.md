---
publish: true
permalink: /Example dataset mapping/AFL Radiocarbon Data mapping/Entity taxa_tree_master.md
created: 2026-07-24T09:34:08.039Z
modified: 2026-09-24T05:44:36.959Z
published: 2026-09-24T05:44:36.959Z
Entity_Name: taxa_tree_master
Type: Fixed Values
Public_ID: "[[taxon_id]]"
Target_Entity: "[[Entity tbl_taxa_tree_genera]]"
Local_Keys:
  - "[[genus_id]]"
Remote_Keys: system_id
status: complete
---

Since this is fixed values, I just created these extra columns, using an internal to this dataset holding value of 1 for the genus\_id:

| New Column Name | Source Column |
| --------------- | ------------- |
| species         | groenlandicus |
| genus\_id        | 1             |

> [!info] The fixed value genus\_id is necessary because a species name has an associated genus name that precedes it (The harp seal is formally called _Pagophilus groenlandicus_)
> Therefore, this key is used to associate the species with the genus.

![[images/Entity taxa_tree_master schema.png]]

---

# YAML

as of 2026-03-23:

```
  name: taxa_tree_master
type: fixed
public_id: taxon_id
keys: []
columns:
  - system_id
  - taxon_id
  - species
  - common_name
  - taxon_common_name_id
values:
  - - 1
    - null
    - null
    - null
    - null
```
