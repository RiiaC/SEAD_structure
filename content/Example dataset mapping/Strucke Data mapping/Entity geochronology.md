---
Entity_Name: geochronology
Type: Data (Derived)
Public_ID: "[[geochron_id]]"
Target_Entity:
Local_Keys:
  - 
  - 
  - 
Remote_Keys:
SEAD_table: "[[tbl_geochronology]]"
status: in progress
publish: true
---
> [!info] the columns of this dataset having to do with geochronology include:
> - c14_age_bp	 = [[age]]
> - c14_error = [[error_older]] and [[error_younger]]
> - d13C	= [[delta_13c]]
> - c14_data_status = this column contains three possible values; `ok`, `c14_data_saknas`, and `orealistiskt_c14_värde` (one example)
> - comment = [[notes]]

- [ ] decide what do with `c14_data_status`. Should it be merged with comment to make a composite note? (e.g.: *"c14_data_status ok, Anltyp grop i slutundersökning. Daterar inte anläggningen utan senare inblandning"* or "*c14_data_saknas, Ej med i avhandlingen*" or "*orealistiskt_c14_värde, Faller helt utanför ramen*")
![[Entity geochronology schema 1.png]]


# YAML as of 2026-08-25
````
name: geochronology
type: entity
system_id: system_id
keys: []
columns:
  - c14_age_bp
  - c14_error
  - d13c
  - c14_data_status
  - site_id
  - fid
public_id: geochron_id
source: datasheet_v9
foreign_keys:
  - entity: dating_labs
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
drop_empty_rows:
  - c14_age_bp

```