---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/Entity location type.md
---

> [!info] the types of locations present in this data set are:

| location\_type\_id | location\_type       |
| ---------------- | ------------------- |
| 1                | Country             |
| 2                | provience           |
| 4                | settlment           |
| 17               | Archaeological site |

Figure out how to accomplish these

- [ ] The entire dataset is Swedish, so all rows can have added `location_type_id = 1` , \`location\_name = Sweden
- [ ] All 25 Swedish provinces are represented in this dataset (sometimes with the name spelled out in full, sometimes as an abbreviation, as shown below), and each should be associated with `location_type_id = 2` , \`location\_name = (contents of the Province column)

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

# YAML as of 2026-08-25

````
name: location_type
type: entity
system_id: system_id
keys: []
columns:
  - socken
  - landskap
  - village_farm
  - raa_id
  - site_type
  - site_id
  - uppdragsnummer
  - fid
public_id: location_type_id
source: datasheet_v9

```
````
