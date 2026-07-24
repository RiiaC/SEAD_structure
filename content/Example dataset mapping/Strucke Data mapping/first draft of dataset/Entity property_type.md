---
Entity_Name: property_type
Type: Fixed Values
Public_ID: "[[property_type_id]]"
Target_Entity:
Local_Keys:
  - 
  - 
  - 
Remote_Keys:
SEAD_table: "[[tbl_property_type]]"
date created: Wednesday, February 18th 2026, 9:38:29 am
status: in progress
---
> [!info] this is an Entity Roger created created 2026-03-03 
> This assigns a value of 1 to all rows with a RAÄ number, and 2 to all rows with a Lämningsnummer

- [x] create a fixed-values entity, assigning the name "property_type" and property_type_id
- [x] create three columns in the Columns cell of the Basic tab: property_type, description, and key_in_data
- [x] in the Fixed Values Data box press ADD ROW and fill in the text "*RAÄ-nummer*" under both **property_type** and **description**, and "*raanr*" (the actual column name in the dataset) under **key_in_data**.
- [x] in the Fixed Values Data box press ADD ROW and fill in the text "*Lämningsnummer*" under both **property_type** and **description**, and "*lamningsnummer*" (the actual column name in the dataset) under **key_in_data**.
 This gives:
````
name: property_type
type: fixed
system_id: system_id
keys: []
columns:
  - system_id
  - property_type_id
  - property_type
  - description
  - key_in_data
public_id: property_type_id
values:
  - - 1
    - null
    - RAÄ-nummer
    - RAÄ-nummer
    - full_raa_nr
  - - 2
    - null
    - Lämningsnummer
    - Lämningsnummer
    - lamningsnummer
```










