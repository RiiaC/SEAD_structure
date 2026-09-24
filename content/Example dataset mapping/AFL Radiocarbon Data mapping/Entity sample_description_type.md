---
publish: true
permalink: /Example dataset mapping/AFL Radiocarbon Data mapping/Entity sample_description_type.md
created: 2026-07-24T09:34:08.013Z
modified: 2026-09-24T05:44:36.933Z
published: 2026-09-24T05:44:36.933Z
Entity_Name: sample_description_type
Type: Fixed Values
Public_ID: "[[sample_description_type_id]]"
SEAD_table: "[[tbl_sample_description_types]]"
date created: Thursday, February 19th 2026, 11:04:54 am
status: change this?
---

Since this is fixed values, I just created these extra columns:

| New Column Name | Source Column                                                             |
| --------------- | ------------------------------------------------------------------------- |
| type\_name       | Biological Age                                                            |
| description     | The (infered) age or development stage of the animal whose bone was dated |

> \[!to do] decide if you want to change this to a combo of tbl\_abundance\_modifications and # tbl\_modification\_types as per Tom's suggestion of 2026-02-19

this?
![[images/Entity sample_description_type schema.png]]
or this?

![[images/Entity abundance modification schema.png]]
