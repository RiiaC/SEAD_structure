---
best_matched_column:
  - "[[Quartz AUTHORS]]"
  - "[[year]]"
aliases:
  - O.
date created: Friday, September 26th 2025, 12:51:21 pm
example_data:
  - Bennike et al., 2008
  - Rundkvist et al., 2004
  - this study
publish: true
---
> [!info] The Source column
> Gives a citation for each sample in the form of author-date or cites "this study" 
> Therefore, this is a good match for both [[Quartz AUTHORS]] and [[year]], which are part of [[tbl_biblio]]

![[Radiocarbon data column O.png]]
# biblio
- [ ] create and fill in a sheet called **biblio** in the [radiocarbon_Glykou_etal_2021_input.xlsx](%5Bradiocarbon_Glykou_etal_2021_input.xlsx%5D(https://umeauniversity.sharepoint.com/:x:/r/sites/SEAD72/Shared%20Documents/Task%20force%20-%20System%20analysis%20of%20radiocarbon%20data/Datasets/AFL/input-data/radiocarbon_Glykou_etal_2021_input.xlsx?d=w34fa6e11a37c4afe9398f92ea68bd11c&csf=1&web=1&e=LaDqOd)) spreadsheet with the following columns
- **system_id** This column is filled incrementally, starting with 1 and is used during the import process to keep track of the data in this sheet, and to cross-reference its connections to the other sheets.
- [[Quartz AUTHORS]] *(fill this information in from the bibliography of the paper(s) provided with the dataset)*
- [[year]] *(fill this information in from the bibliography of the paper(s) provided with the dataset)*
- [[title]] *(fill this information in from the bibliography of the paper(s) provided with the dataset)*
- [[full_reference]] *(fill this information in from the bibliography of the paper(s) provided with the dataset)*
- [[doi]] *(fill this information in, if present, from the bibliography of the paper(s) provided with the dataset)*
- [[isbn]] *(fill this information in, if present, from the bibliography of the paper(s) provided with the dataset)*
- [[notes]] *(fill this information in, if present, from the bibliography of the paper(s) provided with the dataset)*
- [[url]] *(fill this information in, if present, from the bibliography of the paper(s) provided with the dataset)*
- [[biblio_id]] fill this in for any references that already exist in SEAD, using the [[biblio_id]] number on record.
# site references

> [!info] Each of the above publications are associated with one or more sites, once information is entered into the above sheet, it is time to link them (the "relational" part of the database)

- [ ] create and fill in a sheet called **site references** which contains the following columns:
- **system_id** This column is filled incrementally, starting with 1 and is used during the import process to keep track of the data in this sheet, and to cross-reference its connections to the other sheets.
- **[[site_id]]** copy this information from the **system_id** numbers of the **sites** sheet (even if a given site already has a SEAD [site_id](app://obsidian.md/site_id)). (_If it helps to keep track of which ones have been done, you can also add a column to show the corresponding **site_name** on this sheet, but it is not needed for the import process, this column is enough to connect the information for the relational part of the database._)
- **[[biblio_id]]** copy this information from the **system_id** numbers of the **biblio** sheet (even if a given site already has a SEAD [site_id](app://obsidian.md/site_id)). (_If it helps to keep track of which ones have been done, you can also add a column to show the corresponding **site_name** on this sheet, but it is not needed for the import process, this column is enough to connect the information for the relational part of the database._)
- **[[site_reference_id]]** If any of references associated with a site for this dataset has already been entered into SEAD as a site reference (*most likely in the case of sites that are also associated with other datasets in SEAD*), look up its **site_reference_id number and enter it here.**






