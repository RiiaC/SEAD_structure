---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity dating_material.md
created: 2026-09-15T10:31:11.713Z
modified: 2026-09-23T05:19:01.233Z
published: 2026-09-23T05:19:01.233Z
Entity_Name: dating_material
Type: Data (Derived)
Source_entity: "[[Entity superabundance]]"
Public_ID: "[[dating_material_id]]"
columns:
  - "[[element_name]]"
  - "[[material]]"
  - "[[species]]"
  - "[[unique_row_identifer]]"
Target_Entity: "[[Example dataset mapping/Strucke Data-mapping/Entity abundance_element|Entity abundance_element]]"
Local_Keys:
  - element_name
Remote_Keys:
  - element_name
SEAD_table: "[[tbl_dating_material]]"
status: outstanding_question
Target_Entity_2: "[[Z_Not_plotted/original Strucke Data mapping/Entity geochronology|Entity geochronology]]"
Local_Keys_2: "[[unique_row_identifer]]"
Remote_Keys_2: "[[unique_row_identifer]]"
change_it: true
---

> [!info] the "material" column of the Strucke data contains information about the material dated, such as "trakol", or "ben".
> Sometimes there is additional information in the cell which would fall under [[tbl_abundance_modifications]], such as "branda", or "Förkolnat", this information was extracted in the[[Entity superabundance]]
>
> - [ ] figure out why the preview shows only two items

# YAML as of 2026-09-18

````
name: dating_material
type: entity
system_id: system_id
keys: []
columns:
  - species
  - material
  - unique_row_identifier
  - element_name
public_id: dating_material_id
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
      allow_unmatched_left: false
  - entity: geochronology
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
      allow_unmatched_left: false
drop_duplicates: true
check_functional_dependency: false
drop_empty_rows: true
filters:
  - type: query
    query: species=="amulettring"
```
````
