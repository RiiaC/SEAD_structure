---
Entity_Name:
Type:
Public_ID: "[[method_id]]"
Target_Entity:
Local_Keys:
  - 
  - 
  - 
Remote_Keys:
SEAD_table: "[[tbl_methods]]"
status: to troubleshoot
publish: true
---
> [!info] these are all radiocarbon dates

 - [x] create the entity
 - [ ] determine which method from the list at [[tbl_methods#3. Dating by radiometric methods]]  is the best match for this data set. 
       In the meantime, going with 39 = conventional
 - [ ] 







# YAML as of 2026-08-25
````
name: methods
type: entity
system_id: system_id
keys: []
columns:
  - fid
public_id: method_id
source: datasheet_v9
extra_columns:
  method: 39

```