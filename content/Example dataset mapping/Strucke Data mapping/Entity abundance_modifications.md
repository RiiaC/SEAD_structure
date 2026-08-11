---
Entity_Name: abundance_modifications
Type: Data (Derived)
Public_ID: "[[abundance_modification_id]]"
Target_Entity:
Local_Keys:
  - 
  - 
  - 
Remote_Keys:
SEAD_table: "[[tbl_abundance_modifications]]"
status: needs creating
publish: true
---
> [!info] The "material" column of the Strucke data sometimes has additional information in the cell which would fall under [[tbl_abundance_modifications]]:
> - (ej förkolnat)
> - brända
> - obrända
> - obränt
   this information will need to be extracted from this column before data ingestion. None of these are already in SEAD (see [[tbl_modification_types]]), so they will all get new [[modification_type_id]] as well as [[abundance_modification_id]] numbers
   


![[abundance_modifications schema.png]]
