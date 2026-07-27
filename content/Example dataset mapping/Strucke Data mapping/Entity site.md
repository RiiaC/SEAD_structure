---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/Entity site.md
---

> \[!to do] The relevant columns for this dataset relating to site are:
>
> - **village\_farm** = [[site_name]]
> - **longitude** = [[longitude_dd]]
> - **latitude** = [[latitude_dd]]
> - **location\_precision** \*\*=  [[site_location_accuracy]]
> - **site\_id** = Lämningsnummer= [[national_site_identifier]]
>
>   In addition, we have coordinates in the Swedish system, which likely go under [[tbl_site_natgridrefs]]:
> - **northing\_3006**
> - **easting\_3006**

---

- create a data-derived entity sites
- link to this entity from [[Example dataset mapping/Strucke Data mapping/Entity location|Entity location]]
- link to this entity from [[Example dataset mapping/Strucke Data mapping/Entity site_property|Entity site_property]]
- link to this entity from [[Entity site_natgridrefs]] (or wherever else we wind up putting  **northing\_3006** and **easting\_3006**

![[images/Entity site schema.png]]

# YAML for this entity as of 2026-06-29:

```
name: site
type: entity
system_id: system_id
keys: []
columns:
  - village_farm
  - latitude
  - longitude
  - location_precision
  - raa_id
  - site_type
  - site_id
  - uppdragsnummer
  - northing_3006
  - easting_3006
public_id: site_id
source: datasheet
drop_duplicates:
  - site_id
check_functional_dependency: false
drop_empty_rows:
  - site_id
```
