---
publish: true
permalink: /Descriptions of files in the SEAD Teams folder/GitHub SEAD_change_control issue 434.md
---

> [!info]+ This page is a duplicate of the information in the GitHub SEAD\_change\_control issue 434:
> https://github.com/humlab-sead/sead\_change\_control/issues/434

### Data entry errors discovered in SEAD's taxon tables

In the course of working with the list of Strucke "species" (read: _common names_) I discovered that somewhere along the line data entry errors may have crept into SEAD's taxonomi. A few genus/species appear to be attached to the wrong family/order when compared with [GBIF](https://www.gbif.org/)

### A report has been compiled

see [Teams > SEAD > SEAD issues > Missmatches between SEAD species-genra and family-order.xlsx](https://umeauniversity.sharepoint.com/:x:/r/sites/SEAD72/Shared%20Documents/SEAD%20issues/Missmatches%20between%20SEAD%20species-genra%20and%20family-order.xlsx?d=wc10966ba6b994c7e99845d31aad0a018\&csf=1\&web=1\&e=dxIHiy)\
for details.

#### Report contents

For a description of the column names in that table, and how the pivot table should be read, see the documentation here: [Metadata for the spreadsheet SEAD-species-genus-to--family-order-miss-matches.xlsx](https://riiac.github.io/SEAD_structure_Obsidian/Descriptions-of-files-in-the-SEAD-Teams-folder/SEAD-species-genus-to--family-order-miss-matches.xlsx)

### Background

As the Strucke data provides mostly the Swedish common name for the species analysed, it was necessary to create a list of the formal names for species/taxa/family/order are associated with which Swedish term. To expedite this process Johan enlisted the help of an AI with access to a copy of the SEAD database, which prepared a report listing the inferred species/taxa/family/order, indicated which of these are already in SEAD, and the corresponding id numbers for each.

I then took the list of species\_id from that AI output and exported from SEAD the species/taxa/family/order names plus the common\_name and ids for each species (see the **Strucke taxa** sheet in the above spreadsheet). The two lists were then compared in a third Excel file using the formula format "=R2=AG2" to flag where the names or id numbers do or do not match what the AI predicted for the next level. there being some wherein the the species/genus did match, but the family/order did not, I checked them against data in [GBIF](https://www.gbif.org/). For at least one of these, lönn (maple) SEAD appears to be in error, as the family/order on record in SEAD appears to be small, water loving plants, and not trees. Even as a non-biologist, this seems wrong to me.

Therefore, I took the time to check all of those potential miss-matches and highlight them in the above spreadsheet. Knowing that if there is a wrong **family\_id** in **tbl\_taxa\_tree\_genera** it will effect more than one species that share that \*_family\_id_, I chose to make this report in a complete list of all species/taxa/family/order and (common\_name, if any) in SEAD, sorted first by order, and then down the hierarchy, so the flagged miss-matches would sit together. It would also serve as a potential base, if anyone wants to search further for other possible miss-matches.

## Results

There were only a handful of miss-matches between genus-family that have been found in the species present in both the Strucke Data and SEAD. I have checked these by hand, and they are now entered into the report, with the url for each species so that someone else can quickly double check before deciding which of these suggested edits to the database, if any, need to happen.

|genus\_name|probably incorrect family\_name|suggested family name for this genus|
|---|---|---|
|Acer|Acoraceae|Sapindaceae|
|Sambucus|Alismataceae|Viburnaceae|
|Viburnum|Alliaceae|Viburnaceae|
|Allium|Araliaceae|Amaryllidaceae|

If I encounter any other similar problems while working with the Strucke taxa lists, I will return to this and edit it further.

### What needs to happen

1. Someone with a biology background needs to check this work, and decide which suggested edits, if any, need to take place.
2. Make the necessary edits in SEAD to re-assign species to the correct family (Or, if it turns out that any of these marked genus-family matches are correct due to being official synonyms, then leave a note of that here and don't change those in SEAD.)
3. Let me know when this happens, I would appreciate it if we know that these are correct before we ingest the Strucke data.
4. Longer term: Should we check all of the rest of the linkages between the various taxa levels to see if there are more errors than just the ones found in the course of working with the Strucke Data? I imaging it would be possible to write a script to do this that compares SEAD linkages between species/taxa/family/order with those on file in [GBIF](https://www.gbif.org/) or similar.
