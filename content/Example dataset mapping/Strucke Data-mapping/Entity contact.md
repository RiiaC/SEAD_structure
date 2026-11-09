---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity contact.md
created: 2026-11-02T14:43:22.682Z
modified: 2026-11-09T14:05:53.234Z
published: 2026-11-09T14:05:53.234Z
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

- [x] Wait for Roger's reply about how public the contact information stored in the database is
- [x] Get back to Ulf with that answer
- [x] Add the rest of the contact details

# YAML as of 2026-11-09

````
name: contact
type: fixed
system_id: system_id
keys: []
columns:
  - address_1
  - address_2
  - country_location_id
  - email
  - first_name
  - last_name
  - phone_number
  - url
  - town_location_id
public_id: contact_id
values:
  - - 1
    - null
    - null
    - null
    - 205
    - ulf.strucke@gmail.com
    - Ulf
    - Strucke
    - null
    - null
    - null
  - - 2
    - null
    - Engelska parken, Thunbergsvägen 3H, Uppsala University, 751 20 Uppsala
    - Box 626. 751 26 UPPSALA
    - 205
    - sakarias.lindgren@arkeologi.uu.se
    - Sakarias
    - Lindgren
    - null
    - https://www.uu.se/kontakt-och-organisation/personal?query=N22-893
    - 4233
  - - 3
    - null
    - Engelska parken, Thunbergsvägen 3H, Uppsala University, 751 20 Uppsala
    - Box 626. 751 26 UPPSALA
    - 205
    - daniel.lowenborg@arkeologi.uu.se
    - Daniel
    - Löwenborg
    - '0705376093'
    - https://www.uu.se/kontakt-och-organisation/personal?query=N4-37
    - 4233
```
````
