---
publish: true
permalink: /Structure of SEAD/Tables/Columns/species.md
created: 2026-07-24T09:34:40.559Z
modified: 2026-10-23T13:00:00.620Z
published: 2026-10-23T13:00:00.620Z
connected_tables:
  - "[[tbl_taxa_tree_master]]"
column_name: species
data_type: character varying
---

Name of the species or designation for unspecified species (e.g., 'sp.', 'spp.').

> [!note] clarifying conversation with Mattias 2026-10-23:
> Yes, so it is quite obvious when I stop and think about it for a second. Uncertainty essentially means that species-level is unknown. Hence, you record the type of uncertainty in the species field. For instance, Betula nana vs. Betula sp.. In the previous we know the species is "nana" but in the latter it is unknown and indicated as such with "sp.".
>
> This does make for some risk though, since we need to trust that the data submitter writes "sp." in the form we want, and if not catch that and correct it. Probably would be easier with some form of uncertainty table.
>
> Regarding "cf.", that is formatted a bit differently than "sp." and "spp.". In the latter you would write Petters data like "Galium sp.", but if I understand it correctly you would write the former as "Hordeum cf. vulgare" (meaning,  barley that looks like it could be vulgare).
>
> Looking at the Strucke data we also have: cf. Quercus sp.
>
> Not sure if that is the ecological standard, need to check with one of the botanists
>
> Okay, so caught Phil for 3 minutes. "cf." is a bit special, as it needs to map to family, genus, and species level. So there is a table for cf. sp. is only species level however.
