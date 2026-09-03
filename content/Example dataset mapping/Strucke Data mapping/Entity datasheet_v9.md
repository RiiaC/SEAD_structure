---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/Entity datasheet_v9.md
---

> [!info] This entity updated 2026-06-29 to point to `c14_master_v08.xlsx` file, from which the other entities for this dataset will be created. This is, in theory, the final version of the Strucke Data set.

> [!warning] as of the 2026-06-29 update, it is not possible to preview this entity:
> InternalServerError
> 'str' object has no attribute 'project\_name'
> Suggestions:
>
> - Check server logs for details
> - Verify your request parameters are valid
>
> However, it is possible to preview these entities that get their data from this entity:
>
> - site

# YAML as of 2026-08-25

````
name: datasheet_v9
type: openpyxl
system_id: system_id
keys: []
columns:
  - fid
  - socken
  - landskap
  - place_name
  - raa_id
  - site_type
  - site_id
  - uppdragsnummer
  - lab_id
  - c14_age_bp
  - c14_error
  - d13c
  - pmc_value
  - pmc_error
  - c14_data_status
  - comment
  - assessed_relevant
  - material
  - material_edited
  - modifacation
  - species
  - context_id
  - context_type
  - northing_3006
  - easting_3006
  - longitude
  - latitude
  - location_precision
  - cal_68_min
  - cal_68_max
  - cal_95_min
  - cal_95_max
  - median_cal_year
  - calibration_method
  - calibration_status
  - author
  - publication_year
  - title
  - journal
  - place_of_publication
public_id: datasheet_nine_id
options:
  filename: StruckeC14_Sweden_v09.xlsx
  location: local
  sheet_name: StruckeC14_Sweden_v09

```





````
