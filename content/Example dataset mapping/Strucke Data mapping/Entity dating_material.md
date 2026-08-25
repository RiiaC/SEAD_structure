---
Entity_Name: dating_material
Type: Data (Derived)
Public_ID: "[[dating_material_id]]"
Target_Entity: "[[Example dataset mapping/Strucke Data mapping/Entity geochronology|Entity geochronology]]"
Local_Keys:
  - fid
Remote_Keys:
  - fid
SEAD_table: "[[tbl_dating_material]]"
status: to troubleshoot
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




# YAML as of 2026-08-25
````
name: dating_material
type: entity
system_id: system_id
keys: []
columns:
  - material
  - site_id
  - species
  - fid
public_id: dating_material_id
source: datasheet_v9
foreign_keys:
  - entity: geochronology
    local_keys:
      - fid
    remote_keys:
      - fid
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
drop_duplicates:
  - material
check_functional_dependency: false
drop_empty_rows:
  - material

```
