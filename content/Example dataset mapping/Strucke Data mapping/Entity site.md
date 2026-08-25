---
Entity_Name: site
Type: Data (Derived)
Public_ID: "[[site_id]]"
SEAD_table: "[[tbl_sites]]"
status: in progress
publish: true
---
> [!to do] The relevant columns for this dataset relating to site are:
> - **village_farm** = [[site_name]]  
> - **longitude** = [[longitude_dd]]
> - **latitude** = [[latitude_dd]]
> - **location_precision** **=  [[site_location_accuracy]]
> - **site_id** = Lämningsnummer= [[national_site_identifier]]
>   
>   In addition, we have coordinates in the Swedish system, which likely go under [[tbl_site_natgridrefs]]:
> - **northing_3006** 
> - **easting_3006** 

****

- [x] create a data-derived entity sites
- [ ] link to this entity from [[Example dataset mapping/Strucke Data mapping/Entity location|Entity location]]
- [ ] link to this entity from [[Example dataset mapping/Strucke Data mapping/Entity site_property|Entity site_property]]
- [ ] link to this entity from [[Entity site_natgridrefs]] (or wherever else we wind up putting  **northing_3006** and **easting_3006**

![[Entity site schema.png]]

# YAML for this entity as of 2026-08:24:
````
name: site
type: entity
system_id: system_id
keys: []
columns:
  - latitude
  - longitude
  - location_precision
  - raa_id
  - site_type
  - site_id
  - uppdragsnummer
  - northing_3006
  - easting_3006
  - place_name
  - landskap
  - fid
public_id: site_id
source: datasheet_v9
drop_duplicates:
  - site_id
check_functional_dependency: false
drop_empty_rows:
  - site_id

````
