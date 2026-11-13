---
publish: true
permalink: /Structure of SEAD/Tables/index.md
title: Tables
description: Overview of SEAD database tables and their relationships.
created: 2026-07-24T09:34:40.830Z
modified: 2026-11-13T13:11:06.093Z
published: 2026-11-13T13:11:06.093Z
---

# Tables Overview

This section contains descriptions for each of the tables in the SEAD database, as of the date of last export (see [[Code used to create this summary of the Structure of SEAD]]), with properties showing their primary key, any other keys it may have, the columns associated with each table, plus connections to other tables. 

As of 2026-11-13 the tables in this list are grouped into Domains based on the Domains column listing from the [[sead_standard Target Model YAML]] as exported from the [Strucke Data-mapping Shape Shifter project](obsidian://open?vault=SEAD_structure_Obsidian\&file=Example%20dataset%20mapping%2Findex). As a result, there will be some tables in the "Ungrouped" folder that do have Domains defined. They will be sorted into their correct Domains at a later date.

Here is the list of Domains as it appears in that Target Model file. I do not yet know if, for those tables which have more than one Domain listed, the order in which they are listed is meant to convey a hierarchy. However, of the twelve unique Domains in the spreadsheet, ten of them either appear alone, or appear first in the list of two domains that apply to a table, and it happens that a pair of domains appears in both orders (abundance, taxonomy) vs (taxonomy, abundance).

| **Domains**     |                     |
| --------------- | ------------------- |
| abundance       | taxonomy            |
|                 | spatial             |
| analysis        | dating              |
|                 | taxonomy            |
| contacts        | provenance          |
| core            | contacts            |
|                 | excavation          |
|                 | tenprovenance       |
|                 | sample-metadata     |
|                 | spatial             |
| dating          |                     |
| excavation      |                     |
| provenance      | bibliography        |
| sample-metadata | analysis            |
|                 | physical-properties |
|                 | provenance          |
|                 | spatial             |
| spatial         | physical-properties |
|                 | sample-metadata     |
| taxonomy        | abundance           |
