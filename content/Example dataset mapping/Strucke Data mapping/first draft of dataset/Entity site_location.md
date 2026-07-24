---
Entity_Name: site_location
Type: Data (Derived)
Public_ID: "[[site_location_id]]"
Target_Entity: "[[content/Example dataset mapping/Strucke Data mapping/Entity site|Entity site]]"
Local_Keys:
  - "[[site_id]]"
Remote_Keys: system_id
SEAD_table: "[[tbl_site_locations]]"
Target_Entity_2: "[[content/Example dataset mapping/Strucke Data mapping/Entity location|Entity location]]"
Local_Keys_2: "[[location_id]]"
Remote_Keys_2: system_id
status: needs creating
---
> [!to do] This maps the connections between the archaeological sites and their geographic locations.
> The relevant columns for this dataset relating to site and location include
> **- By/Gård** = [[site_name]]  
> - **Socken** + **- RAÄ-nr** =  [[tbl_site_properties]] (where [[tbl_property_type]] = RAÄ nummer)
>  - **Fornlämningstyp** = [[site_description]]
> - **Lämningsnummer** = [[national_site_identifier]]
> - **Uppdragsnummer** =  [[tbl_site_properties]] (where [[tbl_property_type]] = RAÄ nummer)
> 
> The final version of the file will also have two columns for koordinater (WGS 84), which will be the equivalent to:
> -  [[latitude_dd]] 
> - [[longitude_dd]]



![[Entity site schema.png]]


