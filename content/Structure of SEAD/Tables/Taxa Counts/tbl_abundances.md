---
publish: true
permalink: /Structure of SEAD/Tables/Taxa Counts/tbl_abundances.md
---

Records data related to biological proxies, such as individual counts, presence indicators, or scaled values, linking each entry to a specific taxon through an analysis entity. It serves as a species list detailing abundance information for a single physical sample. The intermediate analysis entity allows for the association of multiple proxies per sample. Entries typically reflect count values (abundance), but can also denote presence (1) or use categorical or relative scales, as specified by the dataset's data type.

# my notes 2026-03-27

There are three parent tables to this table:
[[tbl_taxa_tree_master]] This table is obligatory, as the foreign key pointing to it from this table may not be null
[[tbl_analysis_entities]] This table is obligatory, as the foreign key pointing to it from this table may not be null
[[tbl_abundance_elements]] This table is optional, as the foreign key pointing to it from this table may be null (this makes sense, as one can count a whole plant or animal, in which case you don't need to specify the element, just the species.)
