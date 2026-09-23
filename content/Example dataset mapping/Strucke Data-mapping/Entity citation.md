---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity citation.md
created: 2026-09-15T10:31:11.679Z
modified: 2026-09-23T05:19:01.189Z
published: 2026-09-23T05:19:01.189Z
Entity_Name: biblio
Type: Data (Derived)
Source_entity: "[[Example dataset mapping/Strucke Data-mapping/Entity datasheet|Entity datasheet]]"
Public_ID: "[[biblio_id]]"
columns:
  - "[[author]]"
  - "[[journal]]"
  - "[[place_of_publication]]"
  - "[[publication_year]]"
  - "[[title]]"
SEAD_table: "[[tbl_biblio]]"
status: outstanding_question
change_it: true
---

> \[!to do] The relevant columns for this dataset relating to publications for each sample are
>
> - author = [[node_modules/buffer/AUTHORS]]
> - publication\_year = [[year]]
> - title = [[title]]
> - journal =  (no SEAD equivalent, but can be added to [[full_reference]])
> - place of publication =  (no SEAD equivalent, but can be added to [[full_reference]])
>   To make [[full_reference]] combine all of the above using the Extra Columns tab, and the expression `{author} ({publication_year}) {title}, {journal}, {place_of_publication}`

> [!warning] as of 2026-09-18 the above code to make [[full_reference]] gives a warning: "_´full\_reference´ conflicts with an existing or reserved result column_."
> Roger has been asked about this, and will look into it.

# YAML as of 2026-09-17

```
name: citation
type: entity
system_id: system_id
keys:
  - full_reference
columns:
  - author
  - publication_year
  - title
  - journal
  - place_of_publication
public_id: biblio_id
source: datasheet
drop_duplicates: true
check_functional_dependency: false
drop_empty_rows: true
extra_columns:
  full_reference: '{author} ({publication_year}) {title}, {journal}, {place_of_publication}'
  year: '{publication_year}'
```

![[images/Entity biblio schema.png]]
