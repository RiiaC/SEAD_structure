---
Entity_Name: sample_group
Type: Data (Derived)
Public_ID: "[[sample_group_id]]"
Target_Entity: "[[content/Example dataset mapping/Strucke Data mapping/Entity site|Entity site]]"
Local_Keys:
  - site
  - 
Remote_Keys:
  - system_id
SEAD_table: "[[tbl_sample_groups]]"
status: needs creating
---
> [!info] SEAD requires all physical samples to be part of a sample group, even if there is only one sample in the group, as it is the sample group that has the connection to a site. 
> Therefore this layer is added, as an intermediary layer between [[content/Example dataset mapping/Strucke Data mapping/Entity site|Entity site]] and 
> 
> use Labnr as the sample number for joins

needs connections to:
- [ ] [[content/Example dataset mapping/Strucke Data mapping/Entity site|Entity site]]
- [ ] [[content/Example dataset mapping/Strucke Data mapping/first draft of dataset/Entity methods|Entity methods]]
needs connections from 
- [ ] [[content/Example dataset mapping/Strucke Data mapping/Entity physical_samples|Entity physical_samples]]
![[Entity sample_groups schema.png]]





![[Entity Sample Groups.png]]


