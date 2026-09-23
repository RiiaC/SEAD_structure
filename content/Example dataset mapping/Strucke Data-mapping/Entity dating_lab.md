---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity dating_lab.md
created: 2026-09-15T10:31:11.707Z
modified: 2026-09-23T05:19:01.233Z
published: 2026-09-23T05:19:01.233Z
Entity_Name: dating_lab
Type: Fixed Values
Public_ID: dating_lab_id
columns:
  - "[[extracted_lab_prefix]]"
  - "[[manual_prefix]]"
SEAD_table: "[[tbl_dating_labs]]"
status: outstanding_question
change_it: true
---

> [!info] the [[lab_id]] column of the Strucke Data gives both the name of the lab, and the number that lab used to identify the sample.
> Bruno used AI to extract the 54 lab name abbreviation from the [[lab_id]] to [[extracted_lab_prefix]], and then manually edited some of the resulting list in the [[manual_prefix]] column
>
> - [ ] figure out the best way to record the information that Beta/CAMS, Beta/ETH, and Beta/AMS all had their pre-processing done at Beta, and the dating done at the lab in the second half of the name (in the short term, I just copied these terms into the [[manual_prefix]] column)

![[images/Entity dating_labs schema.png]]

# YAML as of 2026-08-25

````
```

````
