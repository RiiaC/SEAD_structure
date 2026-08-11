---
Entity_Name: analysis_entities
Type: Data (Derived)
Public_ID: "[[analysis_entity_id]]"
Target_Entity: "[[Example dataset mapping/Strucke Data mapping/Entity physical_samples|Entity physical_samples]]"
Local_Keys:
  - lab_no
Remote_Keys:
  - lab_no
SEAD_table: "[[tbl_analysis_entities]]"
status: in progress
publish: true
---
> [!info]  The table that records what is actually analysed. 
> In this dataset, perhaps we can simply attach an analysis_entities_id to every row by `labnr` and call it good?

- [x] create the data-derived analysis_entities and select `labn_no` and `material`
- [ ] wait for Roger's response to my message sent 2026-05-05 for the error message I got when I tried to create a join with [[Example dataset mapping/Strucke Data mapping/Entity physical_samples|Entity physical_samples]] on `lab_no`

> [!warning] Do not set either of the joined entities to "drop duplicates", or you will get an error message on the join.



![[Entity analysis_entities schema.png]]


