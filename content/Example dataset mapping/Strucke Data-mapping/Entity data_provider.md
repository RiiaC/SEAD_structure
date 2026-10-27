---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity data_provider.md
created: 2026-10-27T11:56:04.629Z
modified: 2026-10-27T12:01:58.409Z
published: 2026-10-27T12:01:58.409Z
Entity_Name: data_provider
Type:
Source_entity:
Public_ID: data_provider_id
columns:
  - "[[contact_id]]"
  - "[[data_provider_code]]"
  - "[[data_provider_name]]"
Target_Entity:
Local_Keys: []
Remote_Keys:
SEAD_table:
status:
---

> [!info]

# YAML as of 2026-10-27

````
name: data_provider
type: fixed
system_id: system_id
keys:
  - data_provider_code
columns:
  - data_provider_code
  - data_provider_name
  - contact_id
public_id: data_provider_id
column_types:
  data_provider_code: string
  data_provider_name: string
  contact_id: int
values:
  - - 1
    - null
    - strucke
    - Ulf Strucke
    - null

```
````
