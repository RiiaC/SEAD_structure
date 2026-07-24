---
Entity_Name: site
Type: Data (Derived)
Public_ID: "[[location_id]]"
status: in progress
---

> [!info] The relevant columns for this dataset relating to site and location include
> **- socken** = [[location]], where [[location_type]] = 2 (in this case parish)
> **- landskap** = [[location]], where [[location_type]] = 2 (in this case province)
> **- village_farm** = [[site_name]]  
> **- raa_id** = [[site_property]], where [[property_type]] = RAÄ_number
> **- site_type** = [[site_property]], where [[property_type]] = type_of_site
> **- site_id** = Lämningsnummer= [[national_site_identifier]]
> **- uppdragsnummer** = [[site_property]], where [[property_type]] = uppdragsnummer (the official government number on record for a specific Swedish archaeological excavation)
> 
>  Since the entire dataset is Sweden specific, we can also add a column to every row for **Country** ( [[location_type_id]] = 1) and set it to Sweden.




![[Entity site schema.png]]