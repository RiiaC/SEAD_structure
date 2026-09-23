---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity abundance_modification.md
created: 2026-09-15T10:31:11.627Z
modified: 2026-09-23T09:18:49.379Z
published: 2026-09-23T09:18:49.379Z
Entity_Name: abundance_modifications
Type: Data (Derived)
Source_entity: "[[Entity superabundance]]"
Public_ID: "[[abundance_modification_id]]"
columns:
  - "[[abundance_key]]"
  - "[[modification_type]]"
Target_Entity: "[[Example dataset mapping/Strucke Data-mapping/Entity modification_types|Entity modification_types]]"
Local_Keys:
  - "[[modification_type]]"
Remote_Keys:
  - "[[modification_type]]"
SEAD_table: "[[tbl_abundance_modifications]]"
status: complete
Target_Entity_2: "[[Entity abundance]]"
Local_Keys_2: "[[abundance_key]]"
Remote_Keys_2: "[[abundance_key]]"
change_it: true
---

> [!info] The "material" column of the Strucke data sometimes has additional information in the cell which should fall under [[tbl_abundance_modifications]]:
>
> - (ej förkolnat)
> - brända
> - obrända
> - obränt
>   Therefore, the [[modification_type]] column was extracted in the [[Entity superabundance]]m and the [[abundance_key]] used to ensure that each type is properly tied to other information.

> [!note] None of these modifications are already in SEAD (see [[tbl_modification_types]]),
> so they will all get new [[modification_type_id]] as well as [[abundance_modification_id]] numbers.

# schema image

![[images/abundance_modifications schema.png|500]]

# YAML as of 2026-09-17

```
name: abundance_modification
type: entity
system_id: system_id
keys: []
columns:
  - abundance_key
  - modification_type
public_id: abundance_modification_id
source: superabundance
foreign_keys:
  - entity: modification_type
    local_keys:
      - modification_type
    remote_keys:
      - modification_type
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
      allow_unmatched_left: true
  - entity: abundance
    local_keys:
      - abundance_key
    remote_keys:
      - abundance_key
    how: left
    constraints:
      cardinality: one_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
      allow_unmatched_left: true
drop_duplicates: true
check_functional_dependency: false
drop_empty_rows:
  - modification_type
```
