---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/Entity location.md
---

> [!info] The relevant columns for this dataset relating to site and location include
> **- socken** = [[location]], where [[location_type]] = 2 (in this case parish)
> **- landskap** = [[location]], where [[location_type]] = 2 (in this case province)
> **- village\_farm** = [[site_name]]\
> **- raa\_id** = [[site_property]], where [[property_type]] = RAÄ\_number
> **- site\_type** = [[site_property]], where [[property_type]] = type\_of\_site
> **- site\_id** = Lämningsnummer= [[national_site_identifier]]
> **- uppdragsnummer** = [[site_property]], where [[property_type]] = uppdragsnummer (the official government number on record for a specific Swedish archaeological excavation)
>
> Since the entire dataset is Sweden specific, we can also add a column to every row for **Country** ( [[location_type_id]] = 1) and set it to Sweden.

![[images/Entity site schema.png]]
