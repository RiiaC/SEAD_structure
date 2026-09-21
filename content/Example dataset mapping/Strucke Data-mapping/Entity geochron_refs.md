---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity geochron_refs.md
modified: 2026-09-21T04:57:37.050Z
---

> [!info] As the entire dataset is radiocarbon dates, all of the publications that reported those dats count as "geochron refs".
> This table links the reported dates with the reported citations.

![[images/Entity geochron_refs shcema.png|500]]

# YAML as of 2026-09-18

```
name: geochron_refs
type: entity
system_id: system_id
keys: []
columns:
  - unique_row_identifier
  - full_reference
public_id: test_id
source: supergeochron
foreign_keys:
  - entity: geochronology
    local_keys:
      - unique_row_identifier
    remote_keys:
      - unique_row_identifier
    how: inner
    constraints:
      cardinality: one_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
      allow_unmatched_left: true
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
drop_empty_rows:
  - full_reference
```

```




```
