---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/Entity abundances.md
---

> [!info] we don't have counts of the things that were dated, but we do know that at least one something had to be present to have been dated,
> and in SEAD it is the abundances table that become an analysis entity, which in turn has analysis values and/or geochronological results.  Therefore, we need this entity, too.

- create a data-derived entity for abundances
- select `lab_no`, `material`,  `species_1` and `species_2`
  \`
- add an extra column, [[abundance]] and give it always a value of 1, now we have "counted" one for each row

![[images/Entity abundances schema 1.png]]
