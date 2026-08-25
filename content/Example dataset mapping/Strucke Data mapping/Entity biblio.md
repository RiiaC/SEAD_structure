---
Entity_Name: biblio
Type: Data (Derived)
Public_ID: "[[biblio_id]]"
SEAD_table: "[[tbl_biblio]]"
status: in progress
publish: true
---
> [!to do] The relevant columns for this dataset relating to publications for each sample are
> - author = [[node_modules/buffer/AUTHORS]]
> - publication_year = [[year]]
> - title = [[title]]
> - journal =  (no SEAD equivalent, but can be added to [[full_reference]])
> - place of publication =  (no SEAD equivalent, but can be added to [[full_reference]])
> To make [[full_reference]] combine all of the above using the Extra Columns tab, and the expression "{author} {publication_year} {titel} {tidskrift} {publicaiton_city}" (or whatever the column names turn out to be)

- [x] create a data-derived (from [[Entity datasheet_v9|Entity datasheet_v9]]) entity **biblio**, with **biblio_id**
- [x] in the Basic tab choose as Columns: author, publication_year, title, journal, place_of_publication (and village_farm to associate it later to sites)
- [x] add an Extra Column called **full_reference** using {author} {publication_year}{title} {journal} {place_of_publication}
- [x] drop duplicates based on the **full_reference**
- [x] create the [[Example dataset mapping/Strucke Data mapping/Entity site_references|Entity site_references]] and do the join from there



# YAML as of 2026-08-25

````
name: biblio
type: entity
system_id: system_id
keys: []
columns:
  - author
  - publication_year
  - place_of_publication
  - journal
  - title
  - fid
public_id: biblio_id
source: datasheet_v9
drop_duplicates:
  - full_reference
check_functional_dependency: false
extra_columns:
  full_reference: '{forfattare} {tryckar} {titel} {tidskrift} {forlagsort}'
  
  (YAML copied 2026-08-25)
`````




![[Entity biblio schema.png]]