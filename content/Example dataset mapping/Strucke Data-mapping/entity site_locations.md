---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/entity site_locations.md
modified: 2026-09-22T05:51:07.541Z
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
