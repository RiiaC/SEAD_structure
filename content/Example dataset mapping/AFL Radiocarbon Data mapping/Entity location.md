---
Entity_Name: location
Type: Excel File(OpenPyXL)
Public_ID: "[[location_id]]"
Target_Entity: "[[Entity location_type]]"
Local_Keys:
  - "[[location_type_id]]"
Remote_Keys: "[[location_type_id]]"
SEAD_table: "[[tbl_locations]]"
status: complete
---
Since I had already compiled the location information into the locations sheet of the radiocarbon_Glykou_etal_2021_input.xlsx this entity accesses that sheet and imports the columns. In addition the entity is linked to the location_type entity through their common locaiton_type_id columns.

![[Entity location schema.png]]

