---
publish: true
permalink: /Example dataset mapping/AFL Radiocarbon Data mapping/Entity location.md
created: 2026-07-24T09:34:07.968Z
modified: 2026-09-23T05:19:00.050Z
published: 2026-09-23T05:19:00.050Z
Entity_Name: location
Type: Excel File(OpenPyXL)
Public_ID: "[[location_id]]"
Target_Entity: "[[Entity location_type]]"
Local_Keys:
  - "[[location_type_id]]"
Remote_Keys: "[[location_type_id]]"
SEAD_table: "[[tbl_locations]]"
status: complete
change_it: true
---

Since I had already compiled the location information into the locations sheet of the radiocarbon\_Glykou\_etal\_2021\_input.xlsx this entity accesses that sheet and imports the columns. In addition the entity is linked to the location\_type entity through their common locaiton\_type\_id columns.

![[images/Entity location schema.png]]
