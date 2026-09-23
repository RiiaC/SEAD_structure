---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity property_type.md
created: 2026-09-15T10:31:11.804Z
modified: 2026-09-23T05:19:01.366Z
published: 2026-09-23T05:19:01.366Z
Entity_Name: property_type
Type: Fixed Values
Public_ID: property_type_id
columns:
  - "[[description]]"
  - "[[property_type_name]]"
  - "[[value_class_id]]"
  - "[[value_type_id]]"
SEAD_table: "[[property_type]]"
status: outstanding_question
change_it: true
---

> [!info] in order to use the new [[tbl_site_properties]] table, we need to define the [[property_type]]s

- [ ] figure out what Bruno meant to do with the [[value_type_id]] and [[value_class_id]] columns he added

# YAML as of 2026-09-21

````
name: property_type
type: fixed
system_id: system_id
keys: []
columns:
  - system_id
  - property_type_id
  - property_type_name
  - description
  - value_type_id
  - value_class_id
  - uuid
public_id: property_type_id
column_types:
  property_type_name: string
  description: string
  value_type_id: int
  value_class_id: int
values:
  - - 1
    - 1
    - raä nummer
    - null
    - null
    - null
    - null
  - - 2
    - 2
    - type of site
    - null
    - null
    - null
    - null
  - - 3
    - 3
    - uppdragsnummer
    - null
    - null
    - null
    - null
  - - 4
    - 4
    - lämningsnummer
    - null
    - null
    - null
    - null
```

````
