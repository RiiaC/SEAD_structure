---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity species.md
created: 2026-09-16T13:49:39.544Z
modified: 2026-09-24T06:25:06.749Z
published: 2026-09-24T06:25:06.749Z
Entity_Name: species
Type: Data (Derived)
Source_entity: "[[Entity superabundance]]"
Public_ID: "[[taxon_id]]"
columns:
  - "[[species_split]]"
Target_Entity: "[[Entity species_resolution]]"
Local_Keys:
  - "[[species_split]]"
Remote_Keys:
  - "[[species_split]]"
SEAD_table: "[[tbl_taxa_tree_master]]"
status: complete
Target_Entity_2: "[[Example dataset mapping/Strucke Data-mapping/Entity taxa_tree_master|Entity taxa_tree_master]]"
Local_Keys_2: "[[species_split]]"
Remote_Keys_2: "[[species_split]]"
---

> [!info] This entity takes the [[species_split]] output column from the [[Entity superabundance]] and links it to both the [[Entity species_resolution]] and [[Example dataset mapping/Strucke Data-mapping/Entity taxa_tree_master|Entity taxa_tree_master]]

# YAML as of 2026-09-24

```
name: species
type: entity
system_id: system_id
keys: []
columns:
  - species_split
public_id: taxon_id
source: superabundance
foreign_keys:
  - entity: species_resolution
    local_keys:
      - species_split
    remote_keys:
      - species_split
    how: left
    constraints:
      cardinality: one_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
      allow_unmatched_left: true
  - entity: taxa_tree_master
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
drop_duplicates: true
check_functional_dependency: false
drop_empty_rows:
  - species_split
```
