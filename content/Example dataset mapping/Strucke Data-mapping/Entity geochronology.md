---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity geochronology.md
created: 2026-09-15T10:31:11.739Z
modified: 2026-09-23T05:19:01.250Z
published: 2026-09-23T05:19:01.250Z
Entity_Name: geochronology
Type: Data (Derived)
Source_entity: "[[Example dataset mapping/Strucke Data-mapping/Entity supergeochron|Entity supergeochron]]"
Public_ID: "[[geochron_id]]"
columns:
  - "[[c14_age]]"
  - "[[c14_error]]"
  - "[[comment]]"
  - "[[d13C]]"
  - "[[lab_id]]"
  - "[[lab_prefix_raw]]"
  - "[[unique_row_identifer]]"
Target_Entity: "[[Entity dating_lab]]"
Local_Keys:
  - "[[lab_prefix_raw]]"
Remote_Keys:
  - "[[extracted_lab_prefix]]"
SEAD_table: "[[tbl_geochronology]]"
status: outstanding_question
Target_Entity_2: "[[Entity analysis_entity]]"
Local_Keys_2: "[[unique_row_identifer]]"
Remote_Keys_2: "[[unique_row_identifer]]"
extra_columns:
  - "[[age]]"
  - "[[delta_13c]]"
  - "[[error_older]]"
  - "[[error_younger]]"
  - "[[Structure of SEAD/Columns/lab_number]]"
  - "[[notes]]"
change_it: true
---

> [!info] These are columns of this dataset having to do with geochronology. They are linked to SEAD's column names by setting the Extra Columns to:
>
> - [[lab_id]] = [[Structure of SEAD/Columns/lab_number]]
> - [[c14_age_bp]] = [[age]]
> - [[c14_error]] = [[error_older]] and [[error_younger]]
> - [[d13C]]	= [[delta_13c]]
> - comment = [[notes]]

- [ ] decide what do with [[c14_data_status]],  which contains only three different values; `ok`, `c14_data_saknas`, and `orealistiskt_c14_värde` (the last one has only one example in the data set). Should it be merged with comment to make a composite note? (e.g.: _"c14\_data\_status ok, Anltyp grop i slutundersökning. Daterar inte anläggningen utan senare inblandning"_ or "_c14\_data\_saknas, Ej med i avhandlingen_" or "_orealistiskt\_c14\_värde, Faller helt utanför ramen_")
  ![[images/Entity geochronology schema 1.png]]

# YAML as of 2026-09-18

````
name: geochronology
type: entity
system_id: system_id
keys:
  - lab_id
  - unique_row_identifier
columns:
  - c14_age_bp
  - d13c
  - c14_error
  - comment
  - unique_row_identifier
  - lab_id
  - lab_prefix_raw
public_id: geochron_id
source: supergeochron
foreign_keys:
  - entity: dating_lab
    local_keys:
      - lab_prefix_raw
    remote_keys:
      - extracted_lab_prefix
    how: left
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
      allow_unmatched_left: true
      allow_null_keys: false
  - entity: analysis_entity
    local_keys:
      - unique_row_identifier
    remote_keys:
      - unique_row_identifier
    how: inner
    constraints:
      cardinality: one_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
      allow_unmatched_left: true
drop_duplicates: true
check_functional_dependency: false
extra_columns:
  lab_number: '{lab_id}'
  age: '{c14_age_bp}'
  error_older: '{c14_error}'
  error_younger: '{c14_error}'
  delta_13c: '{d13c}'
  notes: '{comment}'
```
````
