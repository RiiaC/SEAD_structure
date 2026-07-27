---
publish: true
permalink: /Example dataset mapping/AFL Radiocarbon Data mapping/Entity sample_descriptions.md
---

I created this extra column with which to do the join.

| New Column Name     | Source Column |
| ------------------- | ------------- |
| description\_type\_id | 1             |
Note: There are only six different sorts of biological age in this dataset, which get reused for every sample for which they apply. While we could use the "drop duplicates" function to assign a unique system\_id numbers to each of these, Roger feels this is not needed, as this is a descriptive field, and future datasets may have more variety in what they report for biological age.

| biological\_age |
| -------------- |
| nd             |
| 0-3 m          |
| 3-10 m         |
| subadult       |
| adult          |
| juvenile       |

> \[!to do] decide if you want to change this to a combo of tbl\_abundance\_modifications and # tbl\_modification\_types as per Tom's suggestion of 2026-02-19

this?
![[images/Entity sample_description_type schema.png]]
or this?

![[images/Entity abundance modification schema.png]]
