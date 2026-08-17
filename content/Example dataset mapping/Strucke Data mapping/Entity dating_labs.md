---
Entity_Name: dating_labs
Type: Data (Derived)
Public_ID: dating_lab_id
Target_Entity:
Local_Keys:
  - 
  - 
  - 
Remote_Keys:
SEAD_table: "[[tbl_dating_labs]]"
status: in progress
publish: true
---
> [!info] the lab-no column of the Strucke Data gives both the name of the lab, and the number that lab used to identify the sample.

- [x] make a data derived Shape Shifter entity looking at the `lab_no` column
- [ ] extract the [[international_lab_id]] from each `lab_no`
- [ ] assign the correct SEAD [[dating_lab_id]] to each row of the Strucke Data from that information
- [ ] if there are any labs not already present in SEAD, gent them a new `dating_lab_id` number
- [ ] for those lab numbers with no easily recognisable labs, figure out if we want to leave dating labs blank, or ask someone to figure out what the lab was based on the publication, or...?





