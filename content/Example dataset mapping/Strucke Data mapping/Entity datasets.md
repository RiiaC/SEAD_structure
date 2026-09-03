---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/Entity datasets.md
---

> [!info] Gives a name to the full dataset, in this case: _Strucke data_

- [x] create the fixed-value entity **datasets** with **dataset\_id**
  on the Basic tab
- [x] under Columns, add **dataset\_name**
- [x] under Fixed Values Data press ADD ROW
- [x] enter "_Strucke data_" under **dataset\_name**
- [x] join to [[Example dataset mapping/Strucke Data mapping/Entity methods|Entity methods]] on the `fid`
- [ ] later, when Sakarias and colleagues publish the paper based on this dataset, it can be added and linked with the foreign key bibilo\_id for that paper in [[Example dataset mapping/Strucke Data mapping/Entity biblio|Entity biblio]]
- [ ] wait for reply to chat of 2026-03-11 06:57 before deciding if we need an entity for [[tbl_data_types]]

![[images/Entity datasets schema.png]]

# YAML as of 2026-08-25

````
name: dataset
type: entity
system_id: system_id
keys: []
columns:
  - fid
public_id: dataset_id
source: datasheet_v9
foreign_keys:
  - entity: methods
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
extra_columns:
  dataset_name: Strucke Data

```
````
