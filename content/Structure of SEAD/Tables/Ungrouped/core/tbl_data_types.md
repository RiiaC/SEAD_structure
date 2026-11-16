---
publish: true
permalink: /Structure of SEAD/Tables/Ungrouped/core/tbl_data_types.md
created: 2026-07-24T09:34:40.968Z
modified: 2026-11-16T12:26:44.328Z
published: 2026-11-16T12:26:44.328Z
table_name: tbl_data_types
primary_key: "[[data_type_id]]"
columns:
  - "[[data_type_name]]"
  - "[[date_updated]]"
  - "[[definition]]"
foreign_keys:
  - "[[data_type_group_id]]"
connected_tables:
  - "[[tbl_data_type_groups]]"
required: No
role: classifier
domain:
  - core
---

> [!abstract] Controlled vocabulary for the type of data produced by an analytical method.
> Specifies the types of quantification methods used in datasets, including definitions of each classification system.

The below list of data types (as of ) is sorted by groups, as defined by the **data\_type\_group\_id**

# 1. Continuous data types

| [[data_type_id]] | [[data_type_name]]     | [[definition]]                                                                         |
| ---------------- | ---------------------- | -------------------------------------------------------------------------------------- |
| 8                | Continuous             | A measured quantity.                                                                   |
| 46               | Mixed-method dependent | Multiple datatypes from one method. (e.g. multiple isotope types from masspectrometry) |

# 2. Discrete data types

| data\_type\_id | data\_type\_name | definition                                                                                               |
| ------------ | -------------- | -------------------------------------------------------------------------------------------------------- |
| 5            | Abundance      | The absolute number of the counted element (e.g. seeds fossils) present in the sample.                   |
| 9            | MNI            | Minimum Number of Individual organisms as calculated from recorded parts (e.g. whole insect equivalents) |

# 3. Classification data types

| data\_type\_id | data\_type\_name | definition                                                                            |
| ------------ | -------------- | ------------------------------------------------------------------------------------- |
| 19           | Categorical    | Data classified according to a set of predefined categories (e.g. temperature classes |

# 4. Presence only

| data\_type\_id | data\_type\_name | definition                                                                                                   |
| ------------ | -------------- | ------------------------------------------------------------------------------------------------------------ |
| 6            | Presence       | The element/fossil is present in the sample but not quantified (numerical classification where 1 = presence) |

# 5. Relative scale data types

| data\_type\_id | data\_type\_name           | definition                                                                                        |
| ------------ | ------------------------ | ------------------------------------------------------------------------------------------------- |
| 7            | Spot test interpretation | The relative intensity of a spot test result on a three grade scale: 12 3 where 3 is the highest. |
| 20           | Percentage               | Data expressed as a percentage (i.e. out x of 100)                                                |

# 7. Composite scale data types

| data\_type\_id | data\_type\_name            | definition                                                                                                                                                                                        |
| ------------ | ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 10           | Partial abundance         | A legacy data type used in BugsCEP to represent partially quantified and incomplete lists e.g. quantified up to 50 individuals and then estimated.                                                |
| 13           | Undefined other           | Data type is not clearly defined could be a combination of quantification presence/absence and semi-quantification or qualification. Beware of using data of this type for quantification.        |
| 18           | Categorical & Scaled (0-5 | Mix of data specified on a scale of 0 to 5 where 0 is absence and 5 is maximum amount of property and data classified on the presence of a property (e.g. Granite = tempering by granite present) |

# 8. Chronological data types

| data\_type\_id | data\_type\_name     | definition                                                                                                                  |
| ------------ | ------------------ | --------------------------------------------------------------------------------------------------------------------------- |
| 14           | Uncalibrated dates | Sample ages in uncalibrated values consisting of mean and error (+/-). Requires calibration to compare with calendar years. |
| 15           | Counted dates      | Sample ages derived from counted rings layers or dated events.                                                              |
| 16           | Calendar dates     | sample ages calibrated to calendar dates                                                                                    |

# 19. Geographical data types

| data\_type\_id | data\_type\_name       | definition                                                                                                                            |
| ------------ | -------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| 43           | Estimated Years      | Dates that are an estimation                                                                                                          |
| 44           | Composite date       | A date which may include other information than the age such as season terminus and/or error margin.                                  |
| 45           | Approximate location | Geographical location given as approximate values or text. May include multiple levels text strings and exclusions (e.g. not Poland). |
