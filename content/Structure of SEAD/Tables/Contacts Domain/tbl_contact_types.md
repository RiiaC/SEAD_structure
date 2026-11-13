---
publish: true
permalink: /Structure of SEAD/Tables/Contacts Domain/tbl_contact_types.md
created: 2026-07-24T09:34:41.528Z
modified: 2026-11-12T07:11:37.610Z
published: 2026-11-12T07:11:37.610Z
table_name: tbl_contact_types
primary_key: "[[contact_type_id]]"
columns:
  - "[[contact_type_name]]"
  - "[[date_updated]]"
  - "[[description]]"
required: No
role: classifier
domain:
  - contacts
---

> [!info] Controlled vocabulary describing a contact's role in a dataset or project context.
> Specifies various contact types, categorizing them by their roles or functions such as laboratory, sample taker, or dataset creator. This categorization aids in linking contacts to their respective roles within the system.

| **[[contact_type_id]]** | **[[contact_type_name]]**       | **[[description]]**                                              |
| ----------------------- | ------------------------------- | ---------------------------------------------------------------- |
| 1                       | Identified by                   | Specimens identified by contact                                  |
| 2                       | Analysed by                     | Data produced through analytical means by contact                |
| 3                       | Samples processed by            | Samples processed by contact                                     |
| 4                       | Samples taked by                | Samples taken by contact                                         |
| 5                       | Specimen repository             | Specimens are stored at this location                            |
| 6                       | Dataset imported by             | Dataset uploaded to SEAD by this contact                         |
| 7                       | Dataset originally digitised by | Original storage in a database by this contact                   |
| 8                       | Specimen location               | Specimens identified in this dataset are stored at this location |

> [!question] 2026-11-12 I asked Roger for clarification:
> is it type 8 that we would assign to Ulf Strucke for compiling the dataset?
> Is type 6 meant to be our internal person who worked on the dataset import (me/you/ etc...), or is that meant to be the databae provider?
