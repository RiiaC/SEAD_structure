---
Entity_Name: location_type
Type: Data (Derived)
Public_ID: "[[location_type_id]]"
Target_Entity:
Local_Keys:
  - 
  - 
  - 
Remote_Keys:
SEAD_table: "[[tbl_location_types]]"
status: needs creating
publish: true
---
> [!info] the types of locations present in this data set are:
> 

| location_type_id | location_type       |
| ---------------- | ------------------- |
| 1                | Country             |
| 2                | provience           |
| 4                | settlment           |
| 17               | Archaeological site |

The entire dataset is Swedish, so all rows can have added `location_type_id = 1` , `location_name = Sweden

All 25 Swedish provinces are represented in this dataset, and each should be associated with `location_type_id = 2` , `location_name = (contents of the Province column)

| abbreviation | Province name |
| ------------ | ------------- |
|              | Blekinge      |
| Bo           | Bohuslän      |
|              | Dalarna       |
|              | Dalsland      |
|              | Gotland       |
|              | Gästrikland   |
| Ha           | Halland       |
|              | Hälsingland   |
|              | Härjedalen    |
|              | Jämtland      |
|              | Lappland      |
| Me           | Medelpad      |
|              | Norrbotten    |
| Nä           | Närke         |
| Sk           | Skåne         |
| Sm           | Småland       |
| Sö           | Södermanland  |
| Up           | Uppland       |
|              | Värmland      |
|              | Västerbotten  |
| vg           | Västergötland |
| Vs           | Västmanland   |
|              | Ångermanland  |
|              | Öland         |
| Ög           | Östergötland  |

