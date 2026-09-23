---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity site.md
created: 2026-09-15T10:31:11.820Z
modified: 2026-09-22T14:34:27.817Z
published: 2026-09-22T14:34:27.817Z
Entity_Name: site
Type: Data (Derived)
Source_entity: "[[Entity supersite|Entity supersite]]"
Public_ID: "[[site_id]]"
columns:
  - "[[lamningsnummer_1]]"
  - "[[latitude]]"
  - "[[location_precision]]"
  - "[[longitude]]"
  - "[[place_name_fallback_raw]]"
  - "[[place_name]]"
  - "[[site_key]]"
SEAD_table: "[[tbl_sites]]"
status: complete
extra_columns:
  - "[[place_name_resolved]]"
---

> \[!to do] The relevant columns for this dataset relating to site are:
>
> - [[place_name]] = [[site_name]]
> - [[longitude]] = [[longitude_dd]]
> - [[latitude]] = [[latitude_dd]]
> - [[location_precision]]   [[site_location_accuracy]]
> - [[site_id]] = [[Lämningsnummer]] = [[national_site_identifier]]
>
>   In addition, we have coordinates in the Swedish system, which could go under [[tbl_site_natgridrefs]]:
> - **northing\_3006**
> - **easting\_3006**
>   However, as these can be calculated from latitude and longitude, we will not retain them as per SEAD policy for not storing information that can be calculated from other information in the same data set.

Since some sites are missing a [[place_name]], we decided to use the [[site_key]] information for the ones that don't have one.  This was accomplished in steps:
In the [[Entity supersite]]:

- the [[site_key]] was defined in as being made up of all of the information from the columns: [[location_precision]], [[latitude]], [[longitude]], [[raa_id]], [[site_type]], [[uppdragsnummer]], [[socken]], [[landskap]], [[site_id]], [[place_name]]
- the [[place_name_fallback_raw]] was defined as being the same as [[site_key]]
  In this Entity:
- the extra column [[place_name_resolved]] is defined by the code `=coalesce(place_name, place_name_fallback_raw)`

![[images/Entity site schema.png]]

# YAML for this entity as of 2026-09-22

```
name: site
type: entity
system_id: system_id
keys:
  - site_key
columns:
  - place_name
  - longitude
  - latitude
  - lamningsnummer_1
  - place_name_fallback_raw
  - location_precision
  - site_key
public_id: site_id
source: supersite
drop_duplicates:
  - site_key
check_functional_dependency: false
extra_columns:
  place_name_resolved: '=coalesce(place_name, place_name_fallback_raw)'
```
