---
publish: true
permalink: /Structure of SEAD/Tables/Ungrouped/tbl_data_type_groups.md
created: 2026-07-24T09:34:41.528Z
modified: 2026-09-23T05:19:12.366Z
published: 2026-09-23T05:19:12.366Z
table_name: tbl_data_type_groups
primary_key: "[[data_type_group_id]]"
columns:
  - "[[data_type_group_name]]"
  - "[[date_updated]]"
  - "[[description]]"
date created: Friday, September 19th 2025, 3:37:16 pm
change_it: true
---

Contains classifications for various data types, such as relative scale and semi-quantitative.

|data\_type\_group\_id|data\_type\_group\_name|description|
|---|---|---|
|1|Continuous|Systems based on the assumption that data can assume any numerical value.|
|2|Discrete|Systems based on distinct and separate integer values (123...) from a numerical sequence. This is the standard group for biological proxy counts.|
|3|Classification|Any systems based on the division of or estimation of quantities into predefined categories either numerical or relative (e.g. 1-10 few many). In statistical terms this group covers ordinal nominal and categorical data types.|
|4|Presence only|Only the existence of taxa/variables in a sample is recorded as a '1' with no quantity being given. Absence is implicit.|
|5|Relative scale|A loose form of classification where the scale indicates the relative amounts of taxa/variables (123 many). To be avoided if possible.|
|7|Composite scale|Any system which combines two or more forms of counting. E.g. a discrete abundance for small counts and an approximation for super abundant taxa|
|8|Chronological|Data which indicate the age of sample either in relation to an event decay based curve or counted scale.|
|19|Geographical|Geographical data either as a value or as a string.|
