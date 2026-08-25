---
Entity_Name: site
Type: Data (Derived)
Public_ID: "[[location_id]]"
status: in progress
publish: true
SEAD_table: "[[tbl_locations]]"
---

> [!info] The relevant columns for this dataset relating to site and location include
> **- socken** = [[location]], where [[location_type]] = 2 (in this case parish)
> **- landskap** = [[location]], where [[location_type]] = 2 (in this case province)
> **- place_name** = [[site_name]]  
> **- raa_id** = [[site_property]], where [[property_type]] = RAÄ_number
> **- site_type** = [[site_property]], where [[property_type]] = type_of_site
> **- site_id** = Lämningsnummer = [[national_site_identifier]]
> **- uppdragsnummer** = [[site_property]], where [[property_type]] = uppdragsnummer (the official government number on record for a specific Swedish archaeological excavation)
> 
>  Since the entire dataset is Sweden specific, we can also add a column to every row for **Country** ( [[location_type_id]] = 1) and set it to Sweden.

- [x] create data derived entity with the above columns
- [ ] connect to the table as needed to sites and site locations



![[Entity site schema.png]]


# YAML as of 2026-08-25
````
name: location
type: entity
system_id: system_id
keys: []
columns:
  - socken
  - raa_id
  - site_id
  - site_type
  - uppdragsnummer
  - fid
  - place_name
public_id: location_id
source: datasheet_v9

```