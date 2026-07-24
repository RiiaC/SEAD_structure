> [!info]+ The spreadsheet described in this document was created as documentation to accompany https://github.com/humlab-sead/sead_change_control/issues/434
> A copy of the github issue is available in this folder
This is an adaption of the information obtained while creating my [[strucke common names report.xlsx]], but taken into the full [[SEAD complete Taxa info.xlsx]] spreadsheet in the form of some new columns, and a filtered pivot table to report the results.

# the columns in this spreadsheet

| column                     | description                                                                                                                                      |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| [[common_name]]            | the common name (if any) on file in SEAD for this species                                                                                        |
| [[species]]                | the name of the species, as recorded in SEAD                                                                                                     |
| [[genus_name]]             | the name of the genus for this species, as recorded in SEAD                                                                                      |
| [[family_name]]            | the name of the family for this genus, as recorded in SEAD                                                                                       |
| [[order_name]]             | the name of the order for this family, as recorded in SEAD                                                                                       |
| [[taxon_common_name_id]]   | the id number associated with the above common name                                                                                              |
| [[taxon_id]]               | the id number associated with the above species                                                                                                  |
| [[genus_id]]               | the id number associated with the above genus                                                                                                    |
| [[family_id]]              | the id number associated with the above family                                                                                                   |
| [[order_id]]               | the id number associated with the above order                                                                                                    |
| genus-family_miss-match    | the column in which I flag mistakes in the data, using the text *"⚠  missmatch, replace family with:"*                                           |
| suggested_family_for_genus | the name of the family in which this genus actually belongs                                                                                      |
| correct_genus_id           | the genus_id number for the correct genus for this family according to link under source_for_suggestions                                         |
| genus-order miss-match     | a column that can be used if there is a second mistake in this level of connection, otherwise it gets marked with *"none after changing family"* |
| sugested_order_for_genus   | the name of the order in which this genus actually belongs                                                                                       |
| source_for_suggestions     | the URL for the GBIF database entry that supports the suggestion                                                                                 |
# the pivot table report
The pivot table was created by assembling the columns in the "Rows" PivotTable field, in the below order, and applying a filter to genus-family_miss-match to show everything that includes a  ⚠ , sorted by hierarchy, with the order highest. 
Because of the filter, it shows everything under a given order that has the wrong family attached to the genus, but none of the entries that are correctly attached (if any).

| Rows                       |
| -------------------------- |
| [[order_name]]             |
| [[order_id]]               |
| genus-order miss-match     |
| sugested_order_for_genus   |
| [[family_name]]            |
| [[family_id]]              |
| genus-family_miss-match    |
| suggested_family_for_genus |
| [[genus_name]]             |
| [[genus_id]]               |
| [[species]]                |
| [[taxon_id]]               |
| source_for_suggestions     |
| common_name                |
| taxon_common_name_id       |
## screen shot of a report for the various species of maple tree that have the incorrect family in SEAD:
(The coloured text and arrow on the screen shot have been added for clarification)

![[2026-06-23 family-genus miss-match report.png|500]]
This image shows the suggestion that we edit the [[family_id]] for the genus **Acer** (family_id = 3 as currently listed) to point instead to the family **Sapindaceae** (family_id = 157; *see the column `correct_genus_id` for this number, which is not displayed in the pivot table*.) Making this one change to this single row in the `tbl_taxa_tree_families` will correct all ten miss-matches between family and genus, and, since the correct [[family_id]] is correctly tied to the appropriate order, it will also fix all ten miss-matches to of the genus to the order. See the spreadsheet itself at [SEAD species-genus to family-order miss-matches.xlsx](https://umeauniversity.sharepoint.com/:x:/r/sites/SEAD72/Shared%20Documents/SEAD%20issues/SEAD%20species-genus%20to%20%20family-order%20miss-matches.xlsx?d=wc10966ba6b994c7e99845d31aad0a018&csf=1&web=1&e=PBrqSg) for the full reports of all miss-matches found to date.
 