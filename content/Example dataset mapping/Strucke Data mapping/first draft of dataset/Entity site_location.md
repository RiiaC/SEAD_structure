---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/first draft of dataset/Entity site_location.md
---

> \[!to do] This maps the connections between the archaeological sites and their geographic locations.
> The relevant columns for this dataset relating to site and location include
> **- By/Gård** = [[site_name]]
>
> - **Socken** + **- RAÄ-nr** =  [[tbl_site_properties]] (where [[tbl_property_type]] = RAÄ nummer)
> - **Fornlämningstyp** = [[site_description]]
> - **Lämningsnummer** = [[national_site_identifier]]
> - **Uppdragsnummer** =  [[tbl_site_properties]] (where [[tbl_property_type]] = RAÄ nummer)
>
> The final version of the file will also have two columns for koordinater (WGS 84), which will be the equivalent to:
>
> - [[latitude_dd]]
> - [[longitude_dd]]

![[images/Entity site schema.png]]
