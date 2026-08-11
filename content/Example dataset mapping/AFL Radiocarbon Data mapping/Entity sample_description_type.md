---
Entity_Name: sample_description_type
Type: Fixed Values
Public_ID: "[[sample_description_type_id]]"
SEAD_table: "[[tbl_sample_description_types]]"
date created: Thursday, February 19th 2026, 11:04:54 am
status: change this?
publish: true
---
Since this is fixed values, I just created these extra columns:

| New Column Name | Source Column                                                             |
| --------------- | ------------------------------------------------------------------------- |
| type_name       | Biological Age                                                            |
| description     | The (infered) age or development stage of the animal whose bone was dated |


> [!to do] decide if you want to change this to a combo of tbl_abundance_modifications and # tbl_modification_types as per Tom's suggestion of 2026-02-19

this?
![[Entity sample_description_type schema.png]]
 or this?

![[Entity abundance modification schema.png]]