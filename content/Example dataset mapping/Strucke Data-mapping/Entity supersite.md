---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity supersite.md
created: 2026-09-15T10:31:11.864Z
modified: 2026-09-24T05:44:37.455Z
published: 2026-09-24T05:44:37.455Z
Entity_Name: supersite
Type: Data (Derived)
Source_entity: "[[Example dataset mapping/Strucke Data-mapping/Entity datasheet|Entity datasheet]]"
Public_ID:
columns:
  - "[[author]]"
  - "[[context_id]]"
  - "[[context_type]]"
  - "[[journal]]"
  - "[[lab_id]]"
  - "[[landskap]]"
  - "[[latitude]]"
  - "[[location_precision]]"
  - "[[longitude]]"
  - "[[place_name]]"
  - "[[place_of_publication]]"
  - "[[publication_year]]"
  - "[[raa_id]]"
  - "[[site_id]]"
  - "[[site_type]]"
  - "[[socken]]"
  - "[[title]]"
  - "[[unique_row_identifer]]"
  - "[[uppdragsnummer]]"
SEAD_table: N/A
status: complete
---

> [!info] This is an extra entity that Bruno created to accomplish two goals:
>
> 1. split the sites with multiple `site_id` numbers (which is to say more than one lämningsnummer) and/or `uppdragsnummer` into multiple rows, with only one of each sort of these numbers in each
> 2. create a unique `site_key` for each unique site in the dataset, by merging the columns
>
> Doing this step makes it easier to create the linking tables later\*

# the extra columns:

## extracting the extra lamningsnummer from the cells with multiple:

- [[lamningsnummer_1]]:`=trim(regex_extract(site_id, '^[^,]+', 0))` This extracts the first _lamningsnummer_ from the comma separated list when there are multiple _lamningsnummer_ in a single cell.
- [[lamningsnummer_2]]: `=trim(regex_extract(site_id, '^[^,]+,\\s*([^,]+)', 1))` This extracts the second _lamningsnummer_ from the comma separated list when there are multiple _lamningsnummer_ in a single cell.
- [[lamningsnummer_3]]: `=trim(regex_extract(site_id, '^[^,]+,\\s*[^,]+,\\s*([^,]+)', 1))` This extracts the third _lamningsnummer_ from the comma separated list when there are multiple _lamningsnummer_ in a single cell.
- [[lamningsnummer_4]]: `=trim(regex_extract(site_id, '^[^,]+,\\s*[^,]+,\\s*[^,]+,\\s*([^,]+)', 1))` This extracts the forth _lamningsnummer_ from the comma separated list when there are multiple _lamningsnummer_ in a single cell.

# extracting the extra  uppdragsnummer from the cells with multiple:

- [[uppdragsnummer_1]]: `=trim(regex_extract(uppdragsnummer, '^[^,]+', 0))` This extracts the first _uppdragsnummer_ from the comma separated list when there are multiple _uppdragsnummer_ in a single cell.
- [[uppdragsnummer_2]]: `=trim(regex_extract(uppdragsnummer, '^[^,]+,\\s*([^,]+)', 1))` This extracts the second _uppdragsnummer_ from the comma separated list when there are multiple _uppdragsnummer_ in a single cell.
- [[uppdragsnummer_3]]: `=trim(regex_extract(uppdragsnummer, '^[^,]+,\\s*[^,]+,\\s*([^,]+)', 1))` This extracts the third _uppdragsnummer_ from the comma separated list when there are multiple _uppdragsnummer_ in a single cell.

# the code to create the site\_key:

- [[site_key]]: `=concat(location_precision, '|', latitude, '|', longitude, '|', raa_id, '|', site_type, '|', uppdragsnummer, '|', socken, '|', landskap, '|', site_id, '|', place_name)` This takes all of the various parts of site information that together uniquely identify each site, and merges them into one column. This permits a "drop duplicates" that will result in a list of unique sites

## the preparation code to give each site a meaningful place name

- [[place_name_fallback_raw]] = {[[site_key]]}

## the code to make the full reference from the info provided

- [[full_reference]] = {[[site_key]]}-{[[context_id]]}-{[[context_type]]}

## The code to make the sample\_group\_key

- [[sample_group_key]] = {[[site_key]]}-{[[context_id]]}-{[[context_type]]}
  (where each sample group = all samples from the same context layer at the same site)

## the code to make the physical sample key

- [[physical_sample_key]] = {[[sample_group_key]]}-{[[lab_id]]}
-

# YAML as of 2026-09-22

```
name: supersite
type: entity
system_id: system_id
keys:
  - place_name
  - latitude
  - longitude
  - site_description
columns:
  - place_name
  - location_precision
  - latitude
  - longitude
  - raa_id
  - site_type
  - uppdragsnummer
  - socken
  - landskap
  - site_id
  - place_of_publication
  - journal
  - title
  - publication_year
  - author
  - context_type
  - context_id
  - lab_id
  - unique_row_identifier
public_id: transition_site_id
source: datasheet
drop_duplicates: true
check_functional_dependency: false
extra_columns:
  lamningsnummer_1: '=trim(regex_extract(site_id, ''^[^,]+'', 0))'
  lamningsnummer_2: '=trim(regex_extract(site_id, ''^[^,]+,\\s*([^,]+)'', 1))'
  lamningsnummer_3: '=trim(regex_extract(site_id, ''^[^,]+,\\s*[^,]+,\\s*([^,]+)'', 1))'
  lamningsnummer_4: '=trim(regex_extract(site_id, ''^[^,]+,\\s*[^,]+,\\s*[^,]+,\\s*([^,]+)'', 1))'
  uppdragsnummer_1: '=trim(regex_extract(uppdragsnummer, ''^[^,]+'', 0))'
  uppdragsnummer_2: '=trim(regex_extract(uppdragsnummer, ''^[^,]+,\\s*([^,]+)'', 1))'
  uppdragsnummer_3: '=trim(regex_extract(uppdragsnummer, ''^[^,]+,\\s*[^,]+,\\s*([^,]+)'', 1))'
  site_key: '=concat(location_precision, ''|'', latitude, ''|'', longitude, ''|'', raa_id, ''|'', site_type, ''|'', uppdragsnummer, ''|'', socken, ''|'', landskap, ''|'', site_id, ''|'', place_name)'
  place_name_fallback_raw: '{site_key}'
  full_reference: '{author} ({publication_year}) {title}, {journal}, {place_of_publication}'
  sample_group_key: '{site_key}-{context_id}-{context_type}'
  physical_sample_key: '{sample_group_key}-{lab_id}'
```
