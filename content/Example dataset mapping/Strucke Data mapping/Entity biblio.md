---
publish: true
permalink: /Example dataset mapping/Strucke Data mapping/Entity biblio.md
---

> \[!to do] The relevant columns for this dataset relating to publications for each sample are
>
> - author = [[node_modules/buffer/AUTHORS]]
> - publication\_year = [[year]]
> - title = [[title]]
> - journal =  (no SEAD equivalent, but can be added to [[full_reference]])
> - place of publication =  (no SEAD equivalent, but can be added to [[full_reference]])
>   To make [[full_reference]] combine all of the above using the Extra Columns tab, and the expression "{author} {publication\_year} {titel} {tidskrift} {publicaiton\_city}" (or whatever the column names turn out to be)

- create a data-derived (from [[Example dataset mapping/Strucke Data mapping/Entity datasheet|Entity datasheet]]) entity **biblio**, with **biblio\_id**
- in the Basic tab choose as Columns: author, publication\_year, title, journal, place\_of\_publication (and village\_farm to associate it later to sites)
- add an Extra Column called **full\_reference** using {author} {publication\_year}{title} {journal} {place\_of\_publication}
- drop duplicates based on the **full\_reference**
- create the [[Example dataset mapping/Strucke Data mapping/first draft of dataset/Entity site_references|Entity site_references]] and do the joins

```
name: biblio
type: entity
system_id: system_id
keys: []
columns:
  - author
  - publication_year
  - title
  - place_of_publication
  - village_farm
public_id: biblio_id
source: datasheet
drop_duplicates:
  - full_reference
check_functional_dependency: false
extra_columns:
  full_reference: '{author} {publication_year}{title} {journal} {place_of_publication}'

```

![[images/Entity biblio schema.png]]
