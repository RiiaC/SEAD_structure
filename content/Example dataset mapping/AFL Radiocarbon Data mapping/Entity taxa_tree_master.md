---
publish: true
permalink: /Example dataset mapping/AFL Radiocarbon Data mapping/Entity taxa_tree_master.md
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
