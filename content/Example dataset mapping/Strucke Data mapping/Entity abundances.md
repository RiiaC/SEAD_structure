---
Entity_Name: abundances
Type: Data (Derived)
Public_ID: "[[abundance_id]]"
Target_Entity: "[[content/Example dataset mapping/Strucke Data mapping/Entity analysis_entities|Entity analysis_entities]]"
Local_Keys:
  - labnr
Remote_Keys: labnr
SEAD_table: "[[tbl_abundances]]"
status: in progress
---
> [!info] we don't have counts of the things that were dated, but we do know that at least one something had to be present to have been dated, 
> and in SEAD it is the abundances table that become an analysis entity, which in turn has analysis values and/or geochronological results.  Therefore, we need this entity, too.

- [x] create a data-derived entity for abundances
- [x] select `lab_no`, `material`,  `species_1` and `species_2`
`
- [x] add an extra column, [[abundance]] and give it always a value of 1, now we have "counted" one for each row



![[Entity abundances schema 1.png]]



