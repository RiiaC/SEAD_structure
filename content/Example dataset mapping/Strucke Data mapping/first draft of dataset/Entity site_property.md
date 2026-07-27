---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/first draft of dataset/Entity site_property.md
---

- There are now two site property entities, figure out why and which you want

> [!info] an entity Roger created 2026-03-03
> so that we can have both the RAÄ number and Lämnings number so that both sorts of information can be included as properties of the site
>
> _However, Roger later decided that we need a whole new table, so this approach has been abandoned as of 2026-06-29, when the [[Example dataset mapping/Strucke Data mapping/Entity site_property|Entity site_property]] was created._

- create entity **site\_property**, with a **site\_propety\_id**
  **in the basic tab:**
- select the columns **lamningsnummer**, **raanr**, and **socken**
  **in the UNNEST tab:**
- Enable Unnest,
- under Value variables choose **lamningsnummer**, **raanr**
  **under Columns to unpivot:**
- set Variable name Column to **property\_type**
- set  Name for the new column containing variable names to **property\_value**
- wait for Roger to figure out how to pull in the **full\_raa\_nu** instead of the **raanr**, ==then edit this==
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
````
