---
Entity_Name: taxa_tree_master
Type: Fixed Values
Public_ID: "[[taxon_id]]"
Target_Entity: "[[Entity tbl_taxa_tree_genera]]"
Local_Keys:
  - "[[genus_id]]"
Remote_Keys: system_id
status: complete
---
Since this is fixed values, I just created these extra columns, using an internal to this dataset holding value of 1 for the genus_id:

| New Column Name | Source Column |
| --------------- | ------------- |
| species         | groenlandicus |
| genus_id        | 1             |
> [!info] The fixed value genus_id is necessary because a species name has an associated genus name that precedes it (The harp seal is formally called *Pagophilus groenlandicus*)
> Therefore, this key is used to associate the species with the genus.

![[Entity taxa_tree_master schema.png]]

---
# YAML
as of 2026-03-23:
````
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