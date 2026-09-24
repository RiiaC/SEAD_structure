---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity supergeochron.md
created: 2026-09-15T10:31:11.857Z
modified: 2026-09-24T07:00:13.773Z
published: 2026-09-24T07:00:13.773Z
Entity_Name: supergeochron
Type: Data (Derived)
Source_entity: "[[Example dataset mapping/Strucke Data-mapping/Entity datasheet|Entity datasheet]]"
Public_ID: "[[transition_geochron_id]]"
columns:
  - "[[author]]"
  - "[[c14_age_bp]]"
  - "[[c14_error]]"
  - "[[comment]]"
  - "[[d13C]]"
  - "[[journal]]"
  - "[[lab_id]]"
  - "[[place_of_publication]]"
  - "[[publication_year]]"
  - "[[title]]"
  - "[[unique_row_identifer]]"
SEAD_table: N/A
status: in progress
extra_columns:
  - "[[full_reference]]"
  - "[[lab_id_prefix_after_slash]]"
  - "[[lab_id_prefix_composite]]"
  - "[[lab_id_prefix_embedded]]"
  - "[[lab_id_prefix_leading]]"
  - "[[lab_id_prefix]]"
  - "[[lab_id_stripped]]"
  - "[[lab_name_raw]]"
  - "[[lab_prefix_raw]]"
---

> [!info] This one creates many new columns in the process of automatically extracting the name of the lab from the [[lab_id]] column of the dataset

- [ ] copy over the full list and fill in their codes

# YAML as of 2026-09-24

````
.
```> [!info] This is an extra entity that Bruno created to make it possible to extract the lab names from the lab_id number and to make the connection to the geochronrefs table easier.
> 
> Note that since Bruno created this, we noticed  that some rows have more than one lab_id number in the same cell, so it will need another step to extract those

This one creates a bunch of new columns, some of which are just a single step towards a later goal

# lab_id_stripped
This one removes "Okänd" from the dataset (because if we don't know the lab number, then it should be null, and because some of the official lab codes happen to use letter pairs that occur in the name "Okänd", and not doing this step would result in assigning that lab, which would be wrong)
# lab_id_prefix_leading
- fill in the explanations for this, and the rest from https://github.com/Br1CM/sead_strucke_data_cleaning/blob/split-archive-current-pipeline/current/docs/shapeshifter_mappings/lab_prefix_replacements.yml
- 
````
