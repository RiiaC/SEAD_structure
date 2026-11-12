---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entities/Entity data_provider.md
created: 2026-10-27T11:56:04.629Z
modified: 2026-11-02T14:26:50.649Z
published: 2026-11-02T14:26:50.649Z
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
SEAD_table: "[[tbl_data_providers]]"
status:
---

> [!info] This is one of the metadata tables needed for this project

- [ ] Get the table structure info for the new [[tbl_data_providers]] and figure out how to connect this entity to the rest of the project

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
