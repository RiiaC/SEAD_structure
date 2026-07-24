---
Entity_Name: feature_types
Type: Data (Derived)
Public_ID: "[[feature_type_id]]"
SEAD_table: "[[tbl_feature_types]]"
status: complete
---

> [!info] the column **Anläggning**, which is the equivalent to [[feature_type_name]], contains over 1000 unique archaeological feature types, all in Swedish. This in contrast to the more than 600 archaeological feature types already in SEAD in English.

- [x] create the data-derived entity feature_types, with a primary key of feature_type_id
- [x] tell it to consider the columns Anlnr and Anläggning, dropping all duplicates and empty rows for Anläggning to obtain a complete list of the feature types in the dataset


> [!warning] there is also a column **Fornlämningstyp** 
> which contains 294 different terms describing the type of find. Some of these are certainly duplicates with minor spelling differences (*Skärvstanshög vs Skärvstenshög*) or (*Område med skogabrukslämningar vs Område med skogsbrukslämningar vs Område med skogsbrukslämnngar vs Område med skogsbrykslämningar*), while others are incorrectly entered data (*RT90 651130.246, 1547667.704*) or (*L2013:292*) or (*L2022:5614*)

![[Entity feature_types schema.png]]




