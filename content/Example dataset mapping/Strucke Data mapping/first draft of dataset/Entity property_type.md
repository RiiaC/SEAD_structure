---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/first draft of dataset/Entity property_type.md
---

> [!info] this is an Entity Roger created created 2026-03-03
> This assigns a value of 1 to all rows with a RAÄ number, and 2 to all rows with a Lämningsnummer

- create a fixed-values entity, assigning the name "property\_type" and property\_type\_id
- create three columns in the Columns cell of the Basic tab: property\_type, description, and key\_in\_data
- in the Fixed Values Data box press ADD ROW and fill in the text "_RAÄ-nummer_" under both **property\_type** and **description**, and "_raanr_" (the actual column name in the dataset) under **key\_in\_data**.
- in the Fixed Values Data box press ADD ROW and fill in the text "_Lämningsnummer_" under both **property\_type** and **description**, and "_lamningsnummer_" (the actual column name in the dataset) under **key\_in\_data**.
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










````
