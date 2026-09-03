---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/Entity property_type.md
---

> [!info] in order to use the new [[tbl_site_properties]] table, we need to define the [[property_type]]s

Roger created me this entity before heading on vacation with the intent that it will assign `property_type` RAÅ number to each row with data in the raa\_number column, and `property_type` = Lämningsnummer to each row with data in the lämningsummer column

# YAML as of 2026-08-25

````
name: property_type
type: fixed
system_id: system_id
keys: []
columns:
  - system_id
  - property_type_id
  - property_type
  - description
  - key_in_data
public_id: property_type_id
values:
  - - 1
    - null
    - null
    - null
    - null
  - - 2
    - null
    - null
    - null
    - null

```

````
