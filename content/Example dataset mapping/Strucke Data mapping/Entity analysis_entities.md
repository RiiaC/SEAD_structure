---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/Entity analysis_entities.md
---

> [!info]  The table that records what is actually analysed.
> In this dataset, perhaps we can simply attach an analysis\_entities\_id to every row by `labnr` and call it good?

- [x] create the data-derived analysis\_entities and select `labn_no` and `material`
- [ ] wait for Roger's response to my message sent 2026-05-05 for the error message I got when I tried to create a join with [[Example dataset mapping/Strucke Data mapping/Entity physical_samples|Entity physical_samples]] on `lab_id`

> [!warning] Do not set either of the joined entities to "drop duplicates", or you will get an error message on the join.

![[images/Entity analysis_entities schema.png]]

# YAML as of 2026-08-25

````
name: analysis_entities
type: entity
system_id: system_id
keys: []
columns:
  - material
  - lab_id
  - fid
public_id: analysis_entities_id
source: datasheet_v9
foreign_keys:
  - entity: physical_samples
    local_keys:
      - lab_id
    remote_keys:
      - lab_id
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true

```
````
