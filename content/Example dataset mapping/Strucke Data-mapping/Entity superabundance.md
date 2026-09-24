---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity superabundance.md
created: 2026-09-15T10:31:11.849Z
modified: 2026-09-24T06:53:21.475Z
published: 2026-09-24T06:53:21.475Z
Entity_Name: superabundance
Type: Data (Derived)
Source_entity: "[[Example dataset mapping/Strucke Data-mapping/Entity datasheet|Entity datasheet]]"
Public_ID: transition_id
columns:
  - "[[material]]"
  - "[[species]]"
  - "[[unique_row_identifer]]"
SEAD_table: N/A
status: complete
---

> [!info] This is an extra entity that Bruno created to make it possible two split multiple species, elements, and modification types into different rows
> The important thing here is the [[abundance_key]], a unique id for everything we need to count (so for the rows with 6 species, each of them will be counted once)

# new columns

This one creates a bunch of new columns, some of which are just a single step towards a later goal that will be used in other entities.

| Input columns          | created columns                                                              |
| ---------------------- | ---------------------------------------------------------------------------- |
| [[material]]           | `element_name`, [[modification_type]]                                        |
| `species`              | `species_1`, `species_2`, `species_3`, `species_4`, `species_5`, `species_6` |
| `unique_row_identifer` | [[abundance_key]]                                                            |
|                        |                                                                              |

## [[abundance_key]]

uses `{unique_row_identifier}-{element_name}-{species_split}-{modification_type}`to add the info from the other new columns to the `unique_row_identifer` to enable us to still have a unique row identifier after pulling each species in the same cell into their own rows (and duplicating all of the information associated with those rows)

## [[species_1]] to species\_6

uses `=trim(regex_extract(lower(species), '^([^,]+)', 1))` to pull the first species from a list of them in a single cell
(repeats with slightly different code to extract the next species in the list, up to `species_6`, because there are that many in one of them!)

## [[element_name]]

uses `=regex_extract(trim(replace(replace(replace(replace(replace(replace(replace(replace(lower(trim(material)),'(ej förkolnat)',''),'förkolnat',''),'obrända',''),'obränt',''),'brända',''),'  ', ' '),' ,', ','),',,', ',')),'^[,;\s]*(.*?)[,;\s]*$', 1)` to delete from the `material` column the words that describe "modifications" to the material (the item was burned, not burned, etc.), leaving behind only the word describing the material itself (träkol, ben, etc.)

## [[modification_type]]

uses `=regex_extract(replace(replace(concat(coalesce(regex_extract(lower(trim(material)), '\(ej förkolnat\)'), ''), ',',coalesce(regex_extract(lower(trim(material)), '(?<!ej )förkolnat'), ''),',',coalesce(regex_extract(lower(trim(material)), 'obrända'), ''),',', coalesce(regex_extract(lower(trim(material)), 'obränt'),''),',',coalesce(regex_extract(lower(trim(material)), '(?<!o)brända'), '')),',,', ','),',,', ','),'^,*(.*?),*$',1)`  to extract from the `material` column the words that describe "modifications" to the material (the item was burned, not burned, etc.)

## [[abundance_key]]

uses `{unique_row_identifier}-{element_name}-{species_split}-{modification_type}` to interpolate a unique key for each thing that will be counted in [[tbl_abundances]]

# Unnest tab

This one uses some of the above columns to create new rows for each unique species from a single row, without losing any of its associated data

| boxes to fill in                                                                | columns assigned                                                                                     |
| ------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| ID Variables<br>(Columns to keep as-is)                                         | [[species]]<br>[[unique_row_identifer]]<br>[[element_name]]<br>[[material]]<br>[[modification_type]] |
| Value Variables<br>(Columns to unpivot)<br>                                     | [[species_1]] to `species_6`                                                                         |
| Variable Name Column<br>(Name for the new column containing variable names)<br> | [[species_number]]                                                                                   |
| Value Name Column<br>(Name for the new column containing values)<br>            | [[species_split]]                                                                                    |

> [!note] See also Bruno's documentation notes for [Reproducing Manual Resolution Cleaning in ShapeShifter ](https://github.com/Br1CM/sead_strucke_data_cleaning/blob/split-archive-current-pipeline/current/docs/shapeshifter_guide.md)

# YAML as of 2026-09-16

```
name: superabundance
type: entity
system_id: system_id
keys: []
columns:
  - material
  - species
  - unique_row_identifier
public_id: transition_id
source: datasheet
filters:
  - type: query
    stage: after_unnest
    query: species_split.notna() or species_number == 'species_1'
unnest:
  id_vars:
    - species
    - unique_row_identifier
    - element_name
    - material
    - modification_type
  value_vars:
    - species_1
    - species_2
    - species_3
    - species_4
    - species_6
    - species_5
  var_name: species_number
  value_name: species_split
extra_columns:
  species_1: '=trim(regex_extract(lower(species), ''^([^,]+)'', 1))'
  species_2: '=trim(regex_extract(lower(species), ''^[^,]+,\s*([^,]+)'', 1))'
  species_3: '=trim(regex_extract(lower(species), ''^[^,]+,\s*[^,]+,\s*([^,]+)'', 1))'
  species_4: '=trim(regex_extract(lower(species), ''^[^,]+,\s*[^,]+,\s*[^,]+,\s*([^,]+)'', 1))'
  species_5: '=trim(regex_extract(lower(species), ''^[^,]+,\s*[^,]+,\s*[^,]+,\s*[^,]+,\s*([^,]+)'', 1))'
  species_6: '=trim(regex_extract(lower(species), ''^[^,]+,\s*[^,]+,\s*[^,]+,\s*[^,]+,\s*[^,]+,\s*([^,]+)'', 1))'
  element_name: '=regex_extract(trim(replace(replace(replace(replace(replace(replace(replace(replace(lower(trim(material)),''(ej förkolnat)'',''''),''förkolnat'',''''),''obrända'',''''),''obränt'',''''),''brända'',''''),''  '', '' ''),'' ,'', '',''),'',,'', '','')),''^[,;\s]*(.*?)[,;\s]*$'', 1)'
  modification_type: '=regex_extract(replace(replace(concat(coalesce(regex_extract(lower(trim(material)), ''\(ej förkolnat\)''), ''''), '','',coalesce(regex_extract(lower(trim(material)), ''(?<!ej )förkolnat''), ''''),'','',coalesce(regex_extract(lower(trim(material)), ''obrända''), ''''),'','', coalesce(regex_extract(lower(trim(material)), ''obränt''),''''),'','',coalesce(regex_extract(lower(trim(material)), ''(?<!o)brända''), '''')),'',,'', '',''),'',,'', '',''),''^,*(.*?),*$'',1)'
  [[abundance_key]]: '{unique_row_identifier}-{element_name}-{species_split}-{modification_type}'
```
