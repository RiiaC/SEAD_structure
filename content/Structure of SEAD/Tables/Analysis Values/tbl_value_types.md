---
publish: true
permalink: /Structure of SEAD/Tables/Analysis Values/tbl_value_types.md
---

Specifies actual type of values belonging to a value class

| [[value_type_id]] | [[unit_id]] | [[data_type_id]] | name                | base\_type | description                                  |
| ----------------- | ----------- | ---------------- | ------------------- | --------- | -------------------------------------------- |
| 0                 | NULL        | NULL             | Not used            | text      | Not used                                     |
| 1                 | NULL        | 5                | Count               | integer   | An (positive) integer result of an analysis  |
| 2                 | NULL        | 5                | BigCount            | integer   | An (positive) integer result of an analysis  |
| 3                 | NULL        | NULL             | Boolean             | boolean   | A boolean (true/false/yes,no) value          |
| 4                 | NULL        | 20               | Percentage          | decimal   | Percentage of something                      |
| 5                 | NULL        | NULL             | Age in years        | integer   | Age of something in years                    |
| 6                 | 8           | NULL             | Year                | integer   | A calendar year                              |
| 7                 | NULL        | NULL             | Note                | text      | A note of something                          |
| 8                 | NULL        | NULL             | Label               | text      | A designation of something                   |
| 9                 | NULL        | NULL             | Identifier          | text      | An identification of something               |
| 10                | 8           | NULL             | Year range          | int4range | A range of years                             |
| 11                | NULL        | 8                | Measurement         | decimal   | A decimal measurement result of an analysis. |
| 12                | NULL        | 19               | Early/Latewood      | category  | Dendro: Early/Latewood                       |
| 13                | NULL        | 19               | Waney edge (W)      | category  | Dendro: Waney edge (W)                       |
| 17                | NULL        | 19               | Molecular sex       | category  | Molecular sex                                |
| 16                | NULL        | 19               | Damage treatment    | category  | Type of damage treatment                     |
| 15                | NULL        | 19               | SNP capture         | category  | Type of SNP capture.                         |
| 14                | NULL        | 19               | Library preparation | category  | Type of sequence library preparation         |
