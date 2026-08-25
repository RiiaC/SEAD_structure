---
Entity_Name: physical_samples
Type: Data (Derived)
Public_ID: "[[physical_sample_id]]"
Target_Entity:
Local_Keys:
  - 
  - 
  - 
Remote_Keys:
SEAD_table: "[[tbl_physical_samples]]"
status: in progress
publish: true
---
- [ ] needs connection to [[Example dataset mapping/Strucke Data mapping/first draft of dataset/Entity sample_groups|Entity sample_groups]]
- [ ] needs connections to [[Example dataset mapping/Strucke Data mapping/Entity analysis_entities|Entity analysis_entities]]
- [ ] needs connections to [[Entity physical_sample_features]]






![[Entity physical_samples schema.png]]


# YAML as of 2026-08-25
````
name: physical_samples
type: entity
system_id: system_id
keys: []
columns:
  - lab_id
  - fid
public_id: physical_sample_id
source: datasheet_v9

```