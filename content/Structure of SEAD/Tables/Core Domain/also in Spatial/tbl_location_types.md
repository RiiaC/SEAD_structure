---
publish: true
permalink: /Structure of SEAD/Tables/Core Domain/also in Spatial/tbl_location_types.md
created: 2026-07-24T09:34:41.052Z
modified: 2026-11-16T08:45:27.197Z
published: 2026-11-16T08:45:27.197Z
table_name: tbl_location_types
primary_key: "[[location_type_id]]"
columns:
  - "[[date_updated]]"
  - "[[description]]"
  - "[[location_type]]"
required: Yes
role: classifier
domain:
  - core
  - spatial
---

> [!abstract] Controlled vocabulary for location classification.
> Contains definitions for various geographical terms, specifying their resolution and context (e.g., administrative unit, historical administrative unit, lake, country).

| [[location_type_id]] | [[location_type]]                       |
| -------------------- | --------------------------------------- |
| 1                    | Country                                 |
| 2                    | Sub-country administrative region       |
| 4                    | Settlement                              |
| 5                    | Continent                               |
| 7                    | Aggregate/non-admin geographical region |
| 8                    | Institution                             |
| 9                    | Water body                              |
| 10                   | Street address                          |
| 14                   | Historical administrative unit          |
| 16                   | Geographical area                       |
| 17                   | Archaeological site                     |
| 18                   | Island                                  |
| 19                   | Historical settlement                   |
| 20                   | Unprocessed Bugs Transfer               |
