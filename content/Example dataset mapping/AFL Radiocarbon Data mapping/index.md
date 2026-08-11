---
title: AFL Radiocarbon Data mapping
publish: true
---

# Welcome to The AFL Radiocarbon Dataset Mapping via SEAD Shape Shifter section of this web page

>[!info] This folder contains information pertaining to the ongoing mapping of the AFL Radiocarbon data set to the SEAD database structure. 

This section documents the process of mapping AFL Radiocarbon Dataset to the SEAD database structure prior to importing the data. This data is associated with the paper [Glykou et al 2021](https://www.sciencedirect.com/science/article/pii/S0277379120306636) and was originally delivered as three spreadsheets, one for the radiocarbon results, one for strontium analysis results, and one for carbon results. In April 2026 a revised dataset was provided which reveals connections between these datasets by giving a unique sample name to each harp seal bone that was analysed, as well as specifying the various lab numbers used for different types of analysis, so it is easy to see which samples have undergone multiple types of analysis.

This folder tracks my notes on our transition from using Excel spreadsheets to using [SEAD Shape Shifter ](https://shape-shifter.sead.se/projects/riia-glykou_et_al_2021) to do the mapping. Prior to January 2026 the mapping had been done in Excel, with one sheet for the incoming dataset, and one sheet for each SEAD table into which the data would be imported. Prior to April 2026 each of the three analysis types from this data set were to be processed separately, but now that they have keys to link them, they will be treated as a single data set.

This dataset, which was originally submitted prior to the first implementation of SEAD Shape Shifter, had lacked information on site location . That information was later added manually to a new sheet of the incoming spreadsheet, one line for each unique site. Therefore, this part of the mapping was already complete when the dataset was imported into SEAD Shape Shifter, and we needed only to access that sheet.