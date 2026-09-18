---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity dataset.md
modified: 2026-09-18T06:19:48.614Z
---

> [!info] Gives a name to the full dataset, in this case: _Strucke data_
> Note that SEAD links links a dataset to [[tbl_dataset_masters]], so therefore [[Entity master_dataset]] is also needed
> Bruno hadn't linked this one to [[tbl_methods]], like I did in [[Entity datasets|my version of this dataset]]
>
> - [ ] check to see if Bruno solved the dataset methods another way, possibly with just a fixed values column somewhere?

- [ ] later, when Sakarias and colleagues publish the paper based on this dataset, it can be added to the citations and linked with the foreign key bibilo\_id for that paper in [[Entity citation|Entity citation]]
- [ ] wait for reply to chat of 2026-03-11 06:57 before deciding if we need an entity for [[tbl_data_types]]

![[images/Entity datasets schema.png]]

# YAML as of 2026-09-18

````
name: dataset
type: fixed
system_id: system_id
keys:
  - dataset_name
  - master_set_business_key
columns:
  - system_id
  - dataset_id
  - dataset_name
  - master_set_business_key
  - data_type
public_id: dataset_id
values:
  - - 1
    - null
    - null
    - null
    - null
foreign_keys:
  - entity: master_dataset
    local_keys:
      - master_set_business_key
    remote_keys:
      - business_key
    how: inner
    constraints:
      cardinality: one_to_one
      allow_unmatched_right: false
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
```
````
