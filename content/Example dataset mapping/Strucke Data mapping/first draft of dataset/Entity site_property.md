---
Entity_Name: property_types
Type: Fixed Values
Public_ID: "[[site_property_id]]"
Target_Entity:
Local_Keys:
  - 
  - 
  - 
Remote_Keys:
SEAD_table: "[[tbl_site_properties]]"
date created: Wednesday, February 18th 2026, 9:38:29 am
status: in progress
---
- [ ] There are now two site property entities, figure out why and which you want

> [!info] an entity Roger created 2026-03-03
>  so that we can have both the RAÄ number and Lämnings number so that both sorts of information can be included as properties of the site
>
>*However, Roger later decided that we need a whole new table, so this approach has been abandoned as of 2026-06-29, when the [[content/Example dataset mapping/Strucke Data mapping/Entity site_property|Entity site_property]] was created.*

- [x] create entity **site_property**, with a **site_propety_id**
**in the basic tab:**
- [x] select the columns **lamningsnummer**, **raanr**, and **socken**
 **in the UNNEST tab:** 
- [x] Enable Unnest, 
- [x] under Value variables choose **lamningsnummer**, **raanr**
   **under Columns to unpivot:**
- [x] set Variable name Column to **property_type**
- [x] set  Name for the new column containing variable names to **property_value**
- [ ] wait for Roger to figure out how to pull in the **full_raa_nu** instead of the **raanr**, ==then edit this==
this gives:
````
name: site_property
type: entity
system_id: system_id
keys: []
columns:
  - lamningsnummer
  - raanr
  - socken
public_id: site_property_id
source: datasheet
unnest:
  id_vars: []
  value_vars:
    - lamningsnummer
    - raanr
  var_name: property_type
  value_name: property_value
```