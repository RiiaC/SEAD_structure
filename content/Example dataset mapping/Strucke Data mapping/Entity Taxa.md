---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/Entity Taxa.md
modified: 2026-09-16T14:25:03.313Z
---

> [!info] The "species" column of the Strucke data usually contains the Swedish word for the material dated, which is often a name of a plant or animal.
> However, it also contains many latin names, These will be mapped directly to `taxon_id`
>
> Bruno created an `Entity species`, which takes the `species_split` column from his [[Example dataset mapping/Strucke Data mapping/Entity superabundances]]. He plans to use this to export a spreadsheet with the unique species of the dataset so a data expert can check the work against SEAD
>
> He also plans to add a `species_label` column that someone will need to fill, showing which of the names are a `common_name`, which are `taxa`, and which are `pseudo_species`, so that each can be sorted to the correct SEAD table
