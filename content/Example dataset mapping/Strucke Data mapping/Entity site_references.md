---
Entity_Name: site_references
Type: Data (Derived)
Public_ID: "[[site_reference_id]]"
Target_Entity:
Local_Keys:
  - 
  - 
  - 
Remote_Keys:
SEAD_table: "[[tbl_site_references]]"
status: in progress
publish: true
---
> [!info] This entity compiles a unique list of the references cited in the dataset and matches each to their site(s) 


- [x] create a data-derived entity, and add columns for `site_id` and all of the bibliographic columns
- [x] remove duplicates based on site_id
- [x] add an extra column:
  `full_reference: '{forfattare} {tryckar} {titel} {tidskrift} {forlagsort}'
- [x] join to [[Example dataset mapping/Strucke Data mapping/Entity site|Entity site]] on [[site_id]]
- [x] join to [[Example dataset mapping/Strucke Data mapping/Entity biblio|Entity biblio]] on `fid`
- [ ] ask Roger if `fid` is an ok way to join these
- [ ] check Bruno's work on the reference list to see which, if any references from this dataset are already in SEAD, and if they are, figure out how best enter their [[biblio_id]] here.



![[site_references schema.png|500]]




# YAML as of 2026-08-25
````
name: site_references
type: entity
system_id: system_id
keys: []
columns:
  - site_id
  - author
  - title
  - publication_year
  - place_of_publication
  - journal
  - fid
public_id: site_reference_id
source: datasheet_v9
foreign_keys:
  - entity: site
    local_keys:
      - site_id
    remote_keys:
      - site_id
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
  - entity: biblio
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
drop_duplicates:
  - site_id
check_functional_dependency: false
extra_columns:
  full_reference: '{forfattare} {tryckar} {titel} {tidskrift} {forlagsort}'

```