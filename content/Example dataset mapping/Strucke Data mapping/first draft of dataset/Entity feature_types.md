---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/first draft of dataset/Entity feature_types.md
---

> [!info] the column **Anläggning**, which is the equivalent to [[feature_type_name]], contains over 1000 unique archaeological feature types, all in Swedish. This in contrast to the more than 600 archaeological feature types already in SEAD in English.

- create the data-derived entity feature\_types, with a primary key of feature\_type\_id
- tell it to consider the columns Anlnr and Anläggning, dropping all duplicates and empty rows for Anläggning to obtain a complete list of the feature types in the dataset

> [!warning] there is also a column **Fornlämningstyp**
> which contains 294 different terms describing the type of find. Some of these are certainly duplicates with minor spelling differences (_Skärvstanshög vs Skärvstenshög_) or (_Område med skogabrukslämningar vs Område med skogsbrukslämningar vs Område med skogsbrukslämnngar vs Område med skogsbrykslämningar_), while others are incorrectly entered data (_RT90 651130.246, 1547667.704_) or (_L2013:292_) or (_L2022:5614_)

![[images/Entity feature_types schema.png]]
