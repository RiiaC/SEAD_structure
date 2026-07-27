---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/Entity analysis_entities.md
---

> [!info]  The table that records what is actually analysed.
> In this dataset, perhaps we can simply attach an analysis\_entities\_id to every row by `labnr` and call it good?

- create the data-derived analysis\_entities and select \`labn\_no
- wait for Roger's response to my message sent 2026-05-05 for the error message I got when I tried to create a join with [[Example dataset mapping/Strucke Data mapping/Entity physical_samples|Entity physical_samples]] on `lab_no`

> [!warning] Do not set either of the joined entities to "drop duplicates", or you will get an error message on the join.

![[images/Entity analysis_entities schema.png]]
