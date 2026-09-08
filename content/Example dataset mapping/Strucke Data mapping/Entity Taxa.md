---
Entity_Name: Taxa
Type: Data (Derived)
Public_ID: "[[taxon_id]]"
Target_Entity:
Local_Keys:
  - 
  - 
  - 
Remote_Keys:
SEAD_table: tbl_taxa_tree_master
status: needs creating
publish: true
---
> [!info] The "species" column of the Strucke data usually contains the Swedish word for the material dated, which is often a name of a plant or animal. 
> However, it also contains many latin names, These will be mapped directly to `taxon_id`


