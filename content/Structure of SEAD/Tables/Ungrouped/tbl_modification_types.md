---
table_name: tbl_modification_types
primary_key: "[[modification_type_id]]"
columns:
  - "[[date_updated]]"
  - "[[modification_type_description]]"
  - "[[modification_type_name]]"
publish: true
---

Specifies various modifications or alterations observed in Quaternary or sub-fossils, such as carbonization, mineralization, and fragmentation.

| modification_type_id | modification_type_name           | modification_type_description                                                                                       |
| -------------------- | -------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| 1                    | Carbonised                       | Organic matter converted to carbon, most commonly though heating.                                                   |
| 2                    | Calcified                        | Organic matter replaced by calcium                                                                                  |
| 3                    | Eroded                           | Surface of fossil has been worn away by physical processes, such as sediment abbraision.                            |
| 4                    | Fragmented                       | Fossil is not whole.                                                                                                |
| 5                    | Mineralised (unspecific)         | Organic matter replaced by unspecified mineral(s).                                                                  |
| 6                    | Pyritified                       | Organic matter replaced by pyrite or marcasite.                                                                     |
| 7                    | Discoloured (more than expected) | Expected colour of fossil, considering preservation factors, is of an unexpected colour. E.g. as a result of dying. |
| 8                    | Petrified                        | Organic matter converted to stone by impregnation with silica.                                                      |
| 9                    | Encased in amber                 | Fossil is encapsulated in a piece of amber.                                                                         |
| 10                   | Corroded                         | Surface of fossil has been damage by chemical processes.                                                            |


> [!note] this is the table that Tom Ryan suggests we put things like the estimated "biological age" of an animal that grew the bones:
> The numbers in the first column are my guess as to what the `modification_type_id` will be once these new types exist in SEAD.

| modification_type_id | modification_type_name | modification_type_description                                          |
| -------------------- | ---------------------- | ---------------------------------------------------------------------- |
| 11                   | nd                     | The estimated biological age at death for this bone was not determined |
| 12                   | 0-3 m                  | The estimated biological age at death for this bone was 0 to 3 months  |
| 13                   | 3-10 m                 | The estimated biological age at death for this bone was 3 to 10 months |
| 14                   | neonat                 | The estimated biological age at death for this bone was 'neonatal'     |
| 15                   | juvenile               | The estimated biological age at death for this bone was 'juvenile'     |
| 16                   | subadult               | The estimated biological age at death for this bone was 'subadult'     |
| 17                   | adult                  | The estimated biological age at death for this bone was 'adult'        |
