---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/first draft of dataset/Entity taxa_common_names.md
---

> [!info] the art\_1 and art\_2 columns contain common names of the species that were dated

- create a data-derived entity that has columns for `art_1` and `art_2`
- create an extra column `comnon_name` and fill it with the contents of `art_1`
- create a Foreign Key join to the [[Example dataset mapping/Strucke Data mapping/first draft of dataset/Entity taxa_tree_master|Entity taxa_tree_master]], on the `common_name` column of both
- create an extra column `language_id` and give it a value of 2 (for Swedish)
- create a Foreign Key join to the [[Entity languages]], on the `laungage_id` of both

> [!note]
> Both art\_1 and art\_2 contain common names of taxa.
> When they both have common names, they are for different taxa.
> However, sometimes art\_2 appears to instead be a description or elaboration about the information appearing in art\_1
> Therefore, we should we make an attempt to break art\_1 into two different columns, one for common names of taxa, and one for descriptions and additional information to supplement art\_1 **Question:** what is the best way to approach that?

![[images/Entity taxon_common_name schema.png]]
