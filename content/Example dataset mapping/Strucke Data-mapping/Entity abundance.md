---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity abundance.md
created: 2026-09-15T10:31:11.633Z
modified: 2026-09-29T07:57:46.809Z
published: 2026-09-29T07:57:46.809Z
Entity_Name: abundance
Type: Data (Derived)
Source_entity: "[[Entity superabundance|Entity superabundance]]"
Public_ID: "[[abundance_id]]"
columns:
  - "[[abundance_key]]"
  - "[[element_name]]"
  - "[[species_split]]"
  - "[[unique_row_identifer]]"
Target_Entity: "[[Example dataset mapping/Strucke Data-mapping/Entity abundance_element|Entity abundance_element]]"
Local_Keys:
  - element_name
Remote_Keys: element_name
SEAD_table: "[[tbl_abundances]]"
status: complete
Target_Entity_2: "[[Entity species]]"
Local_Keys_2: species_split
Remote_Keys_2: species_split
Target_Entity_3: "[[Entity analysis_entity|Entity analysis_entity]]"
Local_Keys_3: unique_row_identifier
---

> [!info] we don't have reported counts for the various bits of plants and animals that were dated in the many projects that comprise this dataset,
> but we do know that at least one something had to be present to have been dated. In SEAD it is the [[tbl_abundances]] (the plant or animal that was counted) that is linked to the [[tbl_analysis_entities]], which in turn has analysis values and/or geochronological results.  Therefore, we need this entity, too, and can assign a count of 1 to each analysed item.

# Join 1

Uses the [[element_name]] to tie the counted item to the type of plant or body part mentioned (if any) in the `element_name` column of the original dataset.

# Join 2

uses the [[species_split]] to tie the count of 1 to each of the species analysed for each published date in the dataset.

# Join 3

uses the [[unique_row_identifer]] column to tie the count to every "entity" that was analysed for this dataset.

![[images/Entity abundances schema 1.png]]

# YAML as of 2026-09-29

```
name: abundance
type: entity
system_id: system_id
keys:
  - unique_row_identifier
  - element_name
  - species_split
columns:
  - abundance_key
  - unique_row_identifier
  - element_name
  - species_split
public_id: abundance_id
source: superabundance
foreign_keys:
  - entity: abundance_element
    local_keys:
      - element_name
    remote_keys:
      - element_name
    how: left
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
  - entity: species
    local_keys:
      - species_split
    remote_keys:
      - species_split
    how: left
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
      allow_unmatched_left: true
      allow_null_keys: true
  - entity: analysis_entity
    local_keys:
      - unique_row_identifier
    remote_keys:
      - unique_row_identifier
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
      allow_unmatched_left: true
drop_duplicates: true
check_functional_dependency: false
drop_empty_rows:
  - unique_row_identifier
  - species_split
  - element_name

```
