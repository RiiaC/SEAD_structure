---
Entity_Name: geochronology
Type: Data (Derived)
Public_ID: "[[geochron_id]]"
Target_Entity:
Local_Keys:
  - 
  - 
  - 
Remote_Keys:
SEAD_table: "[[tbl_geochronology]]"
status: in progress
publish: true
---
> [!info] the columns of this dataset having to do with geochronology include:
> - c14_age_bp	 = [[age]]
> - c14_error = [[error_older]] and [[error_younger]]
> - d13C	= [[delta_13c]]
> - c14_data_status = this column contains three possible values; `ok`, `c14_data_saknas`, and `orealistiskt_c14_värde` (one example)
> - comment = [[notes]]

- [ ] decide what do with `c14_data_status`. Should it be merged with comment to make a composite note? (e.g.: *"c14_data_status ok, Anltyp grop i slutundersökning. Daterar inte anläggningen utan senare inblandning"* or "*c14_data_saknas, Ej med i avhandlingen*" or "*orealistiskt_c14_värde, Faller helt utanför ramen*")
![[Entity geochronology schema 1.png]]