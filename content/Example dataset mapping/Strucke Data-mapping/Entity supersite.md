---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity supersite.md
modified: 2026-09-17T15:24:33.605Z
---

> [!info] This is an extra entity that Bruno created to accomplish two goals:
>
> 1. split the sites with multiple `site_id` numbers (which is to say more than one lämningsnummer) and/or `uppdragsnummer` into multiple rows, with only one of each sort of these numbers in each
> 2. create a unique `site_key` for each unique site in the dataset, by merging the columns
>
> Doing this step makes it easier to create the linking tables later\*

# the extra columns:

## extracting the extra lamningsnummer from the cells with multiple:

- **lamningsnummer\_1:** `=trim(regex_extract(site_id, '^[^,]+', 0))` This extracts the first _lamningsnummer_ from the comma separated list when there are multiple _lamningsnummer_ in a single cell.
- **lamningsnummer\_2:** `=trim(regex_extract(site_id, '^[^,]+,\\s*([^,]+)', 1))` This extracts the second _lamningsnummer_ from the comma separated list when there are multiple _lamningsnummer_ in a single cell.
- **lamningsnummer\_3:** `=trim(regex_extract(site_id, '^[^,]+,\\s*[^,]+,\\s*([^,]+)', 1))` This extracts the third _lamningsnummer_ from the comma separated list when there are multiple _lamningsnummer_ in a single cell.
- **lamningsnummer\_4:** `=trim(regex_extract(site_id, '^[^,]+,\\s*[^,]+,\\s*[^,]+,\\s*([^,]+)', 1))` This extracts the forth _lamningsnummer_ from the comma separated list when there are multiple _lamningsnummer_ in a single cell.

# extracting the extra  uppdragsnummer from the cells with multiple:

- **uppdragsnummer\_1:** `=trim(regex_extract(uppdragsnummer, '^[^,]+', 0))` This extracts the first _uppdragsnummer_ from the comma separated list when there are multiple _uppdragsnummer_ in a single cell.
- **uppdragsnummer\_2:** `=trim(regex_extract(uppdragsnummer, '^[^,]+,\\s*([^,]+)', 1))` This extracts the second _uppdragsnummer_ from the comma separated list when there are multiple _uppdragsnummer_ in a single cell.
- **uppdragsnummer\_3:** `=trim(regex_extract(uppdragsnummer, '^[^,]+,\\s*[^,]+,\\s*([^,]+)', 1))` This extracts the third _uppdragsnummer_ from the comma separated list when there are multiple _uppdragsnummer_ in a single cell.

# the code to create  `site_key`:

- **site\_key:** `=concat(location_precision, '|', latitude, '|', longitude, '|', raa_id, '|', site_type, '|', uppdragsnummer, '|', socken, '|', landskap, '|', site_id, '|', place_name)` This takes all of the various parts of site information that together uniquely identify each site, and merges them into one column. This permits a "drop duplicates" that will result in a list of unique sites
