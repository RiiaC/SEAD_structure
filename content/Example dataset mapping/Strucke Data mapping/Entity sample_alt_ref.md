---
Entity_Name: sample_alt_ref
Type: Data (Derived)
Public_ID: "[[sample_alt_ref_id]]"
Target_Entity:
Local_Keys:
  - 
  - 
  - 
Remote_Keys:
SEAD_table: "[[tbl_sample_alt_refs]]"
status: complete
publish: true
---


> [!info] the lab_no column of the Strucke data refers to the number of the lab that did the dating analysis, and corresponds to the [[alt_ref]] column of [[tbl_sample_alt_refs]], where [[alt_ref_type]] =  3 = Lab Number.

- [x] create entity looking at `lab_no` column, and drop any empty rows
- [x] add a column where [[alt_ref_type]] =  3 (Lab Number) for all rows




