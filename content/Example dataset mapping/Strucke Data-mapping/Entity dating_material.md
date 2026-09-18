---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity dating_material.md
modified: 2026-09-18T07:34:30.414Z
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
