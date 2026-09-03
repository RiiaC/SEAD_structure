---
publish: true
permalink: /Example dataset mapping/AFL Radiocarbon Data mapping/AFL Radiocarbon Data spreadsheet/O. Source.md
aliases:
  - O.
---

> [!info] The Source column
> Gives a citation for each sample in the form of author-date or cites "this study"
> Therefore, this is a good match for both [[Quartz AUTHORS]] and [[year]], which are part of [[tbl_biblio]]

![[images/Radiocarbon data column O.png]]

# biblio

- [ ] create and fill in a sheet called **biblio** in the [radiocarbon\_Glykou\_etal\_2021\_input.xlsx](%5Bradiocarbon_Glykou_etal_2021_input.xlsx%5D\(https://umeauniversity.sharepoint.com/:x:/r/sites/SEAD72/Shared%20Documents/Task%20force%20-%20System%20analysis%20of%20radiocarbon%20data/Datasets/AFL/input-data/radiocarbon_Glykou_etal_2021_input.xlsx?d=w34fa6e11a37c4afe9398f92ea68bd11c\&csf=1\&web=1\&e=LaDqOd\)) spreadsheet with the following columns
- **system\_id** This column is filled incrementally, starting with 1 and is used during the import process to keep track of the data in this sheet, and to cross-reference its connections to the other sheets.
- [[Quartz AUTHORS]] _(fill this information in from the bibliography of the paper(s) provided with the dataset)_
- [[year]] _(fill this information in from the bibliography of the paper(s) provided with the dataset)_
- [[title]] _(fill this information in from the bibliography of the paper(s) provided with the dataset)_
- [[full_reference]] _(fill this information in from the bibliography of the paper(s) provided with the dataset)_
- [[doi]] _(fill this information in, if present, from the bibliography of the paper(s) provided with the dataset)_
- [[isbn]] _(fill this information in, if present, from the bibliography of the paper(s) provided with the dataset)_
- [[notes]] _(fill this information in, if present, from the bibliography of the paper(s) provided with the dataset)_
- [[url]] _(fill this information in, if present, from the bibliography of the paper(s) provided with the dataset)_
- [[biblio_id]] fill this in for any references that already exist in SEAD, using the [[biblio_id]] number on record.

# site references

> [!info] Each of the above publications are associated with one or more sites, once information is entered into the above sheet, it is time to link them (the "relational" part of the database)

- [ ] create and fill in a sheet called **site references** which contains the following columns:
- **system\_id** This column is filled incrementally, starting with 1 and is used during the import process to keep track of the data in this sheet, and to cross-reference its connections to the other sheets.
- **[[site_id]]** copy this information from the **system\_id** numbers of the **sites** sheet (even if a given site already has a SEAD [site\_id](app://obsidian.md/site_id)). (_If it helps to keep track of which ones have been done, you can also add a column to show the corresponding **site\_name** on this sheet, but it is not needed for the import process, this column is enough to connect the information for the relational part of the database._)
- **[[biblio_id]]** copy this information from the **system\_id** numbers of the **biblio** sheet (even if a given site already has a SEAD [site\_id](app://obsidian.md/site_id)). (_If it helps to keep track of which ones have been done, you can also add a column to show the corresponding **site\_name** on this sheet, but it is not needed for the import process, this column is enough to connect the information for the relational part of the database._)
- **[[site_reference_id]]** If any of references associated with a site for this dataset has already been entered into SEAD as a site reference (_most likely in the case of sites that are also associated with other datasets in SEAD_), look up its **site\_reference\_id number and enter it here.**
