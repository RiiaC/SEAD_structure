---
publish: true
permalink: /Example dataset mapping/AFL Radiocarbon Data mapping/Entity abundance_element.md
created: 2026-07-24T09:34:07.925Z
modified: 2026-09-23T05:18:59.953Z
published: 2026-09-23T05:18:59.953Z
Entity_Name: abundance_element
Type: Data (Derived)
Public_ID: "[[abundance_element_id]]"
SEAD_table: "[[tbl_abundance_elements]]"
status: complete
change_it: true
---

- [x] remove the entity for dating material, it isn't actually needed for this dataset

> [!info] specifies the sort of bone analysed

This entity corresponds to the [[B. Element]] column in the Radiocarbon data source data file, which lists which sort of bone underwent Radiocarbon dating, and to the `K. Bone` column of the Carbon data spreadsheet

There are 12 types of bones in the raidocarbon data set. Use the _Drop Duplicates,_ and _Drop Empty Rows_ options to create this list:

| system\_id | Element    |
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

```
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
```

![[images/Entity abundance_element schema.png|800]]
