---
foreign_keys:
  - "[[rdb_system_id]]"
Entity_Name: abundances
Type: Data (Derived)
Public_ID: "[[abundance_id]]"
Target_Entity: "[[Entity abundance_element]]"
Local_Keys:
Remote_Keys:
SEAD_table: "[[tbl_abundances]]"
Target_Entity_2: "[[Example dataset mapping/AFL Radiocarbon Data mapping/Entity taxa_tree_master]]"
Local_Keys_2: "[[taxon_id]]"
status: error_to_solve
publish: true
---
- [x] create a data-derived entity and pull in columns for element, biological age, and lab_nr
- [x] add extra columns:
Starting from the assumption that there is one bone for each sample, and the information from the associated paper that all bones in this dataset are from harp seals: I add extra columns, using the internal-to-this-dataset holding value of 1 for `taxon_id` that will. in conjunction to the other entities that use `taxon_id`, add the information that all bones in this dataset are harp seals:

| New Column Name | Source Column |
| --------------- | ------------- |
| abundance       | 1             |
| taxon_id        | 1             |
- [ ] add join to the [[Entity abundance_element]] on the element to fills the [[abundance_element_id]] column of this entity with the appropriate numbers for each bone from the system_id row of the [[Entity abundance_element]] sheet. (*errors for this on 2026-04-22, message sent to Roger*)
- [ ] create a second join to link the various taxa information to the abundances (*waiting for the first join's errors to be solved before attempting this*)

![[Entity abundances schema.png|1000]]
