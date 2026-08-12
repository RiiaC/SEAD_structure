---
Entity_Name: site_references
Type: Data (Derived)
Public_ID: "[[site_reference_id]]"
Target_Entity:
Local_Keys:
  - 
  - 
  - 
Remote_Keys:
SEAD_table: "[[tbl_site_references]]"
status: in progress
publish: true
---
> [!info] This entity compiles a unique list of the references cited in the dataset and matches each to their site(s) 


- [x] create a data-derived entity, and add columns for `site_id` and all of the bibliographic columns
- [x] remove duplicates based on site_id
- [x] add an extra column:
  `full_reference: '{forfattare} {tryckar} {titel} {tidskrift} {forlagsort}'
- [ ] join to [[Example dataset mapping/Strucke Data mapping/Entity site|Entity site]] on [[site_id]]
- [ ] join to [[Example dataset mapping/Strucke Data mapping/Entity biblio|Entity biblio]] on [[full_reference]]
- [ ] check Bruno's work on the reference list to see which, if any references from this dataset are already in SEAD, and if they are, enter their [[biblio_id]] here.



![[site_references schema.png]]



