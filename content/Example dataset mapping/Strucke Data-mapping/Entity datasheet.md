---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity datasheet.md
modified: 2026-09-18T07:01:51.405Z
---

> [!info] This entity reads a csv file,  `StruckeC14_Sweden_v1.csv`,  which has been [published to Zenodo](https://zenodo.org/records/21932353) on 2026-08-14
> This is the entity from which the other entities for this dataset will be created. This is, in theory, the final version of the Strucke Data set.

In addition to the input columns named in the [[Example dataset mapping/Strucke Data-mapping/index|index]] for this section, it also contains an extra column, `unique_row_identifier`, which is comprised of enough of the other columns combined to ensure that each row is uniquely identified, using the code `{lab_id}/{context_id}/{species}/{site_id}`

# YAML as of 2026-09-16

````
name: datasheet
type: csv
system_id: system_id
keys: []
columns:
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
public_id: master_dataset_id
options:
  filename: StruckeC14_Sweden_v1.csv
  location: local
  sep: ','
  encoding: utf-8
drop_duplicates: true
check_functional_dependency: false
extra_columns:
  unique_row_identifier: '{lab_id}/{context_id}/{species}/{site_id}'
```





````
