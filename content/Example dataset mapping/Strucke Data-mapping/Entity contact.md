---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity contact.md
created: 2026-11-02T14:43:22.682Z
modified: 2026-11-03T06:20:29.831Z
published: 2026-11-03T06:20:29.831Z
Entity_Name: contact
Type: Fixed Values
Public_ID: contact_id
columns:
  - "[[address_1]]"
  - "[[address_2]]"
  - "[[email]]"
  - "[[first_name]]"
  - "[[last_name]]"
  - "[[location_id]]"
  - "[[phone_number]]"
  - "[[url]]"
SEAD_table: "[[tbl_contacts]]"
status: in progress
---

> [!info] The contact details for the people who provided the dataset

- [ ] Wait for Roger's reply about how public the contact information stored in the database is
- [ ] Get back to Ulf with that answer
- [ ] Add the rest of the contact details, after you hear from Ulf as to what details they want included

# YAML as of 2026-11-02

````
name: contact
type: fixed
system_id: system_id
keys: []
columns:
  - address_1
  - address_2
  - location_id
  - email
  - first_name
  - last_name
  - phone_number
public_id: contact_id
values:
  - - 1
    - null
    - null
    - null
    - 205
    - null
    - Ulf
    - Strucke
    - null
  - - 2
    - null
    - null
    - null
    - 205
    - null
    - Sakarias
    - Lindgren
    - null
  - - 3
    - null
    - null
    - null
    - 205
    - null
    - Daniel
    - Löwenborg
    - null
```
````
