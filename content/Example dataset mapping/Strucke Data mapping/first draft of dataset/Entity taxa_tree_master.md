---
Entity_Name: taxa_tree_master
Type: Data (Derived)
Public_ID: "[[taxon_id]]"
depends_on: "[[content/Example dataset mapping/AFL Radiocarbon Data mapping/Entity taxa_common_names|Entity taxa_common_names]]"
SEAD_table: "[[tbl_taxa_tree_master]]"
status: awaiting lookup table data
---

> [!note] I need to consult with an expert to create this lookup table:
- [ ] extract the list of all common names from `art_1` and `art_2` and their corresponding `sort` 
- [ ] consult with an expert to determine the correct [[species]], [[taxon_id]], [[record_type_name]], [[record_type_id]] +/- [[record_type_description]] for each and record the information in a file ([Strucke common names etc.xlsx](https://umeauniversity.sharepoint.com/:x:/r/sites/SEAD72/Shared%20Documents/Task%20force%20-%20System%20analysis%20of%20radiocarbon%20data/Datasets/Strucke/Work%20in%20progress/Strucke%20common%20names%20etc.xlsx?d=wba13373237f54e0f91bf8a273b9f5ef6&csf=1&web=1&e=CpZzYo))
- [ ] import the complete file into Shape Shifter
- [ ] choose the columns `species`, `common_name`, `taxa_common_name_id


![[Entity taxon_common_name schema.png|500]]
Note: there are many other tables that connect to taxa_tree_master in SEAD, but as most (all?) are not relevant for this dataset, I choose to re-use the image for taxa_common_names instead of displaying the full set

