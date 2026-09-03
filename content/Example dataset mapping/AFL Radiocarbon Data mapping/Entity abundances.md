---
publish: true
permalink: /Example dataset mapping/AFL Radiocarbon Data mapping/Entity abundances.md
---

- [x] create a data-derived entity and pull in columns for element, biological age, and lab\_nr
- [x] add extra columns:
  Starting from the assumption that there is one bone for each sample, and the information from the associated paper that all bones in this dataset are from harp seals: I add extra columns, using the internal-to-this-dataset holding value of 1 for `taxon_id` that will. in conjunction to the other entities that use `taxon_id`, add the information that all bones in this dataset are harp seals:

| New Column Name | Source Column |
| --------------- | ------------- |
| abundance       | 1             |
| taxon\_id        | 1             |

- [ ] add join to the [[Entity abundance_element]] on the element to fills the [[abundance_element_id]] column of this entity with the appropriate numbers for each bone from the system\_id row of the [[Entity abundance_element]] sheet. (_errors for this on 2026-04-22, message sent to Roger_)
- [ ] create a second join to link the various taxa information to the abundances (_waiting for the first join's errors to be solved before attempting this_)

![[images/Entity abundances schema.png|1000]]
