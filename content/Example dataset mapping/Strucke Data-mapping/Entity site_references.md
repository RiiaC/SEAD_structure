---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity site_references.md
created: 2026-09-15T10:31:11.842Z
modified: 2026-09-24T06:22:53.992Z
published: 2026-09-24T06:22:53.992Z
Entity_Name: site_references
Type: Data (Derived)
Source_entity: "[[Entity supersite|Entity supersite]]"
Public_ID: "[[site_reference_id]]"
columns:
  - "[[full_reference]]"
  - "[[site_key]]"
Target_Entity: "[[Example dataset mapping/Strucke Data-mapping/Entity site|Entity site]]"
Local_Keys:
  - "[[site_key]]"
Remote_Keys:
  - "[[site_key]]"
SEAD_table: "[[tbl_site_references]]"
status: outstanding_question
Target_Entity_2: "[[Entity citation]]"
Local_Keys_2: "[[full_reference]]"
Remote_Keys_2: "[[full_reference]]"
---

> [!info] This entity compiles a unique list of the references cited in the dataset and matches each to their site(s)

- [ ] check Bruno's work on the reference list to see which, if any references from this dataset are already in SEAD, and if they are, figure out how best enter their [[biblio_id]] here.

![[images/site_references schema.png|500]]

# YAML as of 2026-09-24

````
name: site_references
type: entity
system_id: system_id
keys:
  - site_key
  - full_reference
columns:
  - site_key
  - full_reference
public_id: site_reference_id
source: supersite
foreign_keys:
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
  - entity: citation
    local_keys:
      - full_reference
    remote_keys:
      - full_reference
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
```
````
