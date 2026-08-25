---
Entity_Name: site_locations
Type: Data (Derived)
Public_ID: "[[site_location_id]]"
Target_Entity: "[[Example dataset mapping/Strucke Data mapping/Entity site|Entity site]]"
Local_Keys:
  - fid
Remote_Keys:
  - fid
SEAD_table: "[[tbl_site_locations]]"
status: complete
publish: true
Target_Entity_2: "[[Example dataset mapping/Strucke Data mapping/Entity location|Entity location]]"
Local_Keys_2: fid
Remote_Keys_2: fid
---
> [!info] connects [[Example dataset mapping/Strucke Data mapping/Entity site|Entity site]] and [[Example dataset mapping/Strucke Data mapping/Entity location|Entity location]]



![[Entity site schema.png]]

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




