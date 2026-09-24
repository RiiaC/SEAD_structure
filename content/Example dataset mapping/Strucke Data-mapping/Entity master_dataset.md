---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity master_dataset.md
created: 2026-09-18T06:12:27.634Z
modified: 2026-09-24T05:44:37.366Z
published: 2026-09-24T05:44:37.366Z
Entity_Name: master_dataset
Type: Fixed Values
Public_ID: master_set_id
columns:
  - "[[biblio_id]]"
  - "[[business_key]]"
  - "[[contact_id]]"
  - "[[master_name]]"
  - "[[master_notes]]"
  - "[[url]]"
SEAD_table: "[[tbl_dataset_masters]]"
status: complete
---

> [!info] A master dataset _"Represents a major grouping identifier for datasets, typically indicating a contributing database, project, user, or laboratory (e.g., BugsCEP, MAL, Lund Dendro Lab)."_
> for this dataset the:
> [[master_name]] = _"Strucke Radiocarbon collection"_
> [[master_notes]] = "This dataset represents the largest available compilation of radiocarbon dates from archaeological contexts in Sweden, comprising 30,301 entries. A table with parishes where data has been collected is included as CSV. An article describing the data and the compilation process is submitted to the Journal of Open Archaeology Data (JOAD). A link to the article will be provided here upon publication for further information about the dataset. The dataset has been produced by Ulf Strucke in collaboration with the Swedish National Infrastructure for Digital Archaeology, Swedigarch. Funding from SAU forskningsråd, the Swedish Research Council (research grant nr 2021-00161) and the participating organisations of Swedigarch."
> [[contact_id]] = (we should probably list contacts for both Ulf and Sak)
> [[url]] = https://zenodo.org/records/21932353
>
> - [ ] go back and fill in the [[biblio_id]] as soon as it is published, or, perhaps enter it as "in press?"

![[images/Entity master_dataset schema.png]]

# YAML as of 2026-09-18

````
name: master_dataset
type: fixed
system_id: system_id
keys:
  - business_key
columns:
  - system_id
  - master_set_id
  - business_key
  - contact_id
  - biblio_id
  - master_name
  - master_notes
  - url
public_id: master_set_id
values:
  - - 1
    - null
    - null
    - null
    - null
    - null
    - null
    - null
```
````
