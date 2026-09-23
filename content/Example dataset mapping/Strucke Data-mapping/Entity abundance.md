---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity abundance.md
created: 2026-09-15T10:31:11.633Z
modified: 2026-09-23T09:09:52.685Z
published: 2026-09-23T09:09:52.685Z
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
Target_Entity_2: "[[Entity Species]]"
Local_Keys_2: species_split
Remote_Keys_2: species_split
Target_Entity_3: "[[Entity analysis_entity|Entity analysis_entity]]"
Local_Keys_3: unique_row_identifier
change_it: true
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

# YAML as of 2026-08-25

```
name: abundances
type: entity
system_id: system_id
keys: []
columns:
  - species
  - lab_id
  - fid
public_id: abundance_id
source: datasheet_v9
foreign_keys:
  - entity: analysis_entities
    local_keys:
      - lab_no
    remote_keys:
      - lab_no
    how: inner
    constraints:
      cardinality: one_to_many
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
      allow_null_keys: false
      allow_unmatched_left: true
extra_columns:
  abundance: '1'
```
