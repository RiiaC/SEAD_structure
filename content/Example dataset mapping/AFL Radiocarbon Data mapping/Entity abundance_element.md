---
Entity_Name: abundance_element
Type: Data (Derived)
Public_ID: "[[abundance_element_id]]"
SEAD_table: "[[tbl_abundance_elements]]"
status: complete
publish: true
---
- [x] remove the entity for dating material, it isn't actually needed for this dataset

> [!info] specifies the sort of bone analysed

This entity corresponds to the [[B. Element]] column in the Radiocarbon data source data file, which lists which sort of bone underwent Radiocarbon dating, and to the `K. Bone` column of the Carbon data spreadsheet

There are 12 types of bones in the raidocarbon data set. Use the *Drop Duplicates,* and *Drop Empty Rows* options to create this list:

| system_id | Element    |
| --------- | ---------- |
| 1         | Phalanx    |
| 2         | Femur      |
| 3         | Temporal   |
| 4         | Mandibula  |
| 5         | nd         |
| 6         | Humerus    |
| 7         | Scapula    |
| 8         | Fibula     |
| 9         | Vertebra   |
| 10        | Occipitale |
| 11        | Cranium    |
| 12        | Radius     |
# YAML

````
name: abundance_element
type: entity
system_id: system_id
keys: []
columns:
  - element
  - lab_nr
public_id: abundance_element_id
source: datasheet
drop_duplicates:
  - element
check_functional_dependency: false
drop_empty_rows:
  - element
`````




![[Entity abundance_element schema.png|800]]



