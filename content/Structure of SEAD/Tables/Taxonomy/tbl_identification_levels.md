---
publish: true
permalink: /Structure of SEAD/Tables/Taxonomy/tbl_identification_levels.md
created: 2026-07-24T09:34:41.561Z
modified: 2026-10-23T13:31:56.693Z
published: 2026-10-23T13:31:56.693Z
table_name: tbl_identification_levels
primary_key: "[[identification_level_id]]"
columns:
  - "[[date_updated]]"
  - "[[identification_level_abbrev]]"
  - "[[identification_level_name]]"
  - "[[notes]]"
---

Serves as a lookup for taxonomic identification levels, detailing the resolution or uncertainty in identification, such as 'cf. Family', 'cf. Genus', or 'cf. Species'.

> [!note] clarifying comment from Mattias 2026-10-23
> Chatted with Phil and you are looking in the correct place:
> For cf., in SEAD documentation it is written as "c.f.", so if you want to search for it that is what needs to be written. For c.f. you have the lookup table tbl\_identification\_levels, which stores c.f. on different taxa levels (family, genus, species). Then tbl\_abundance\_ident\_levls links this to abundances, and via that to taxa\_tree\_master.
> For sp., spp., ident, and grp you record it in the species field in taxa\_tree\_master. This creates a "pseudo-species" that then indicates uncertainty.

|identification\_level\_id|identification\_level\_name|notes|
|---|---|---|
|1|c.f. Family|Uncertainty at the family level|
|2|c.f. Genus|Uncertainty at the genus level|
|3|c.f. Species|Uncertainty at the species level|
|4|Family|Uncertainty at the family level|
|5|Genus|Uncertainty at the genus level|
|6|Species|Uncertainty at the species level|
