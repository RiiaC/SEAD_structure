---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/entity site_locations.md
created: 2026-09-15T10:31:11.828Z
modified: 2026-09-23T05:19:01.433Z
published: 2026-09-23T05:19:01.433Z
Entity_Name: site_locations
Type: Data (Derived)
Source_entity: "[[Entity supersite|Entity supersite]]"
Public_ID: "[[site_location_id]]"
columns:
  - "[[landskap]]"
  - "[[site_key]]"
  - "[[socken]]"
Target_Entity: "[[Example dataset mapping/Strucke Data-mapping/Entity location]]"
Local_Keys:
  - "[[location_name]]"
Remote_Keys:
  - "[[location_name]]"
SEAD_table: "[[tbl_site_locations]]"
status: complete
Target_Entity_2: "[[Example dataset mapping/Strucke Data-mapping/Entity site|Entity site]]"
Local_Keys_2: "[[site_key]]"
Remote_Keys_2: "[[site_key]]"
change_it: true
---

> [!info] connects [[Example dataset mapping/Strucke Data-mapping/Entity site|Entity site]] and [[Example dataset mapping/Strucke Data-mapping/Entity location|Entity location]]

![[images/Entity site schema.png]]

# YAML as of 2026-09-22

````
name: site_location
type: entity
system_id: system_id
keys:
  - site_key
  - location_name
columns:
  - socken
  - landskap
  - site_key
public_id: site_location_id
source: supersite
foreign_keys:
  - entity: location
    local_keys:
      - location_name
    remote_keys:
      - location_name
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
  - entity: site
    local_keys:
      - site_key
    remote_keys:
      - site_key
    how: inner
    constraints:
      cardinality: one_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
drop_duplicates: true
check_functional_dependency: false
drop_empty_rows: true
unnest:
  id_vars:
    - site_key
  value_vars:
    - socken
    - landskap
  var_name: location_type_column
  value_name: location_name
```




````
