---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity location.md
created: 2026-09-15T10:31:11.764Z
modified: 2026-09-29T08:55:33.151Z
published: 2026-09-29T08:55:33.151Z
Entity_Name: site
Type: Data (Derived)
Source_entity: "[[Example dataset mapping/Strucke Data-mapping/Entity datasheet|Entity datasheet]]"
Public_ID: "[[location_id]]"
columns:
  - "[[landskap]]"
  - "[[socken]]"
SEAD_table: "[[tbl_locations]]"
status: outstanding_question
extra_columns:
  - "[[location_type_id]]"
---

> [!info] The relevant columns for this dataset relating to site and location include
> **- socken** = [[location]], where [[location_type]] = 2 (in this case parish)
> **- landskap** = [[location]], where [[location_type]] = 2 (in this case province)
> **- place\_name** = [[site_name]]\
> **- raa\_id** = [[site_property]], where [[property_type]] = RAÄ\_number
> **- site\_type** = [[site_property]], where [[property_type]] = type\_of\_site
> **- site\_id** = Lämningsnummer = [[national_site_identifier]]
> **- uppdragsnummer** = [[site_property]], where [[property_type]] = uppdragsnummer (the official government number on record for a specific Swedish archaeological excavation)
>
> - Bruno used the extra column [[location_type_id]] =  2 for everything in the dataset
> - [ ] Since the entire dataset is Sweden specific, should we also add a column to every row for **Country** ( [[location_type_id]] = 1) and set it to Sweden?

| location\_type\_id | location\_type       |
| ---------------- | ------------------- |
| 1                | Country             |
| 2                | provience           |
| 4                | settlment           |
| 17               | Archaeological site |

| abbreviation | Province name |
| ------------ | ------------- |
|              | Blekinge      |
| Bo           | Bohuslän      |
|              | Dalarna       |
|              | Dalsland      |
|              | Gotland       |
|              | Gästrikland   |
| Ha           | Halland       |
|              | Hälsingland   |
|              | Härjedalen    |
|              | Jämtland      |
|              | Lappland      |
| Me           | Medelpad      |
|              | Norrbotten    |
| Nä           | Närke         |
| Sk           | Skåne         |
| Sm           | Småland       |
| Sö           | Södermanland  |
| Up           | Uppland       |
|              | Värmland      |
|              | Västerbotten  |
| vg           | Västergötland |
| Vs           | Västmanland   |
|              | Ångermanland  |
|              | Öland         |
| Ög           | Östergötland  |

- [ ] the settlements need to have h `location_type_id = 4`  associated with them
- [ ] the archaeological sites (lämningsnummber and RAÄ nummer) need to have h `location_type_id = 17` associated with them

![[images/Entity site schema.png|500]]

# YAML as of 2026-09-29

````
name: location
type: entity
system_id: system_id
keys:
  - location_name
columns:
  - socken
  - landskap
public_id: location_id
source: datasheet
drop_duplicates:
  - location_name
check_functional_dependency: false
unnest:
  id_vars: []
  value_vars:
    - landskap
    - socken
  var_name: location_type_name
  value_name: location_name
extra_columns:
  location_type_id: 2
```
````
