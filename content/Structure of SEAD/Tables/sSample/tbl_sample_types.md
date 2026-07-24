---
table_name: tbl_sample_types
primary_key: "[[sample_type_id]]"
columns:
  - "[[date_updated]]"
  - "[[source/docs/plugins/Description]]"
  - "[[type_name]]"
date created: Friday, September 19th 2025, 3:37:16 pm
---

Defines the physical form or category of a sample. This can include specific sub-samples related to the sampling method of a sample group, or general bulk samples. Examples include 'Core Subsample', 'Grab Sample', and 'Bulk (Bag) Sample'.

> [! abstract] my suggested edit for this:
> Defines the physical form or category of a sample from a sampling method perspective. Examples include 'Core Subsample', 'Grab Sample', and 'Bulk (Bag) Sample', but also 'Field measurement' and even 'Photograph'. For more specific information about the physical sample itself, see [[tbl_record_types]] and [[ tbl_abundance_elements]]

| sample_type_id | type_name                     | description                                                                                                                                                             |
| -------------- | ----------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1              | Bulk sample                   | Sample in a container such as bag, box.                                                                                                                                 |
| 2              | Kubiena subsample             | Unit of sediment extracted from a kubiena box                                                                                                                           |
| 3              | Core subsample                | Unit of sediment extracted from a core                                                                                                                                  |
| 4              | Monolith subsample            | Unit of sediment extracted from a monolithic soil/peat sample                                                                                                           |
| 5              | Tent trap contents            | Contents of tent trap(s), any trap bulking details in notes.                                                                                                            |
| 6              | Pitfall trap contents         | Contents of pitfall trap(s), any trap bulking details in notes.                                                                                                         |
| 7              | Modern insect collection      | Sample from field sampling or hunting of insects (e.g. contents of a tube)                                                                                              |
| 8              | Modern vegetation collection  | Vegetation survey sample unit.                                                                                                                                          |
| 9              | Unspecified                   | Sample type not known or documented                                                                                                                                     |
| 10             | Dendro cross-cut sample       | Cross-cut disc used for dendrochronology analysis                                                                                                                       |
| 11             | Dendro cross-cut wedge sample | Cross-cut wedge shaped sample used for dendrochronolgy analysis                                                                                                         |
| 12             | Dendro core sample            | Wood core sample used for dendrochronolgy analysis                                                                                                                      |
| 13             | Field measurement             | Values measured in field without physical sample (e.g. metal detector, MS-loop, fluxgate magnetometer)                                                                  |
| 14             | Dating pseudosample           | Virtual sample consisting of aggregated material from multiple samples to bulk up weight for radiocarbon dating (or other dating method)                                |
| 16             | Ceramic sherd                 | A sherd originating from any type of ceramic object                                                                                                                     |
| 20             | Photograph                    | Sample consists of a photograph which has been the basis for measurements (e.g. photograph of dendrochronological cross-section).                                       |
| 21             | Tracing                       | A thin paper is placed on the sample surface and a pencil is used to trace the features (e.g. in dendrochronology used to trace the ring-width pattern onto the paper). |
| 22             | Poster putty                  | Poster putty is applied to the surface of the sample in order to create an imprint (e.g. in dendrochronology used to imprint the ring-width sequence).                  |