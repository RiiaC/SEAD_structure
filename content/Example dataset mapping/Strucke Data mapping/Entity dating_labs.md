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
status: needs creating
publish: true
---
> [!info] the lab-no column of the Strucke Data gives both the name of the lab, and the number that lab used to identify the sample.

- [ ] extract the [[international_lab_id]] from each `lab_no`
- [ ] assign the correct SEAD [[dating_lab_id]] to each row of the Strucke Data from that information





