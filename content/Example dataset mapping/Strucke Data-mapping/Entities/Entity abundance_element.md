---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entities/Entity abundance_element.md
created: 2026-09-15T10:31:11.620Z
modified: 2026-11-11T16:03:31.884Z
published: 2026-11-11T16:03:31.884Z
Entity_Name: abundance_element
Type: Data (Derived)
Source_entity: "[[Entity superabundance|Entity superabundance]]"
Public_ID: "[[abundance_element_id]]"
columns:
  - "[[element_name]]"
SEAD_table: "[[tbl_abundance_elements]]"
status: complete
---

> [!info] This is an intermediate step.
> It simply makes the entity needed to have the [[element_name]] ready to ingest into SEAD,
> and be available to be linked to those other entities that need it

# YAML as of 2026-09-17

````
name: abundance_element
type: entity
system_id: system_id
keys:
  - element_name
columns:
  - element_name
public_id: abundance_element_id
source: superabundance
drop_duplicates: true
check_functional_dependency: false
```
````
