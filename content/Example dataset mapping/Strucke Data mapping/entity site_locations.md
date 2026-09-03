---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/entity site_locations.md
---

> [!info] connects [[Example dataset mapping/Strucke Data mapping/Entity site|Entity site]] and [[Example dataset mapping/Strucke Data mapping/Entity location|Entity location]]

![[images/Entity site schema.png]]

# YAML as of 2026-08-25

````
name: site_locations
type: entity
system_id: system_id
keys: []
columns:
  - fid
  - socken
  - landskap
  - place_name
  - raa_id
  - site_type
  - site_id
public_id: site_location_id
source: datasheet_v9
foreign_keys:
  - entity: location
    local_keys:
      - fid
    remote_keys:
      - fid
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
  - entity: site
    local_keys:
      - fid
    remote_keys:
      - fid
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true

```




````
