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




# YAML as of 2026-08-25
````
name: sample_alt_ref
type: entity
system_id: system_id
keys: []
columns:
  - lab_id
  - fid
public_id: sample_alt_ref_id
source: datasheet_v9
drop_empty_rows:
  - lab_no
extra_columns:
  alt_ref_type: 3

```
