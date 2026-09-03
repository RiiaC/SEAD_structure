---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/Entity physical_samples.md
---

- [ ] needs connection to [[Example dataset mapping/Strucke Data mapping/first draft of dataset/Entity sample_groups|Entity sample_groups]]
- [ ] needs connections to [[Example dataset mapping/Strucke Data mapping/Entity analysis_entities|Entity analysis_entities]]
- [ ] needs connections to [[Entity physical_sample_features]]

![[images/Entity physical_samples schema.png]]

# YAML as of 2026-08-25

````
name: physical_samples
type: entity
system_id: system_id
keys: []
columns:
  - lab_id
  - fid
public_id: physical_sample_id
source: datasheet_v9

```
````
