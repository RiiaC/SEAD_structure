---
Entity_Name: dating_material
Type: Data (Derived)
Public_ID: "[[dating_material_id]]"
Target_Entity:
Local_Keys:
  - 
  - 
  - 
Remote_Keys:
SEAD_table: "[[tbl_dating_material]]"
status: in progress
publish: true
---
> [!info] the "material" column of the Strucke data contains information about the material dated, such as "trakol", or "ben". 

> [!note] Sometimes there is additional information in the cell which would fall under [[tbl_abundance_modifications]], such as "branda", or "Förkolnat", this information will need to be extracted from this column before data ingestion. 

- [x] make the data-derived entity for this looking at the `material` column 
- [x] drop duplicates and empty rows based on the `material` column to get the list of 24 types of material dated
- [ ] figure out how to remove the "modifications" from the materials so that we have only materials left

- Bruno suggests that this code might work:
````
regex_extract(trim(replace(replace(replace(replace(replace(replace(replace(lower(trim(material)),'(ej förkolnat)',''),'obrända',''),'obränt',''),'brända',''),'  ', ' '),' ,', ','),',,', ',')),'^[,;\s](.?)[,;\s]*$',1)
````




