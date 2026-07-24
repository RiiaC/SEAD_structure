---
Entity_Name: biblio
Type: Data (Derived)
Public_ID: "[[biblio_id]]"
SEAD_table: "[[tbl_biblio]]"
status: in progress
---
> [!to do] The relevant columns for this dataset relating to publications for each sample are
> - author = [[authors]]
> - publication_year = [[year]]
> - title = [[title]]
> - journal =  (no SEAD equivalent, but can be added to [[full_reference]])
> - place of publication =  (no SEAD equivalent, but can be added to [[full_reference]])
> To make [[full_reference]] combine all of the above using the Extra Columns tab, and the expression "{author} {publication_year} {titel} {tidskrift} {publicaiton_city}" (or whatever the column names turn out to be)

- [x] create a data-derived (from [[content/Example dataset mapping/Strucke Data mapping/Entity datasheet|Entity datasheet]]) entity **biblio**, with **biblio_id**
- [x] in the Basic tab choose as Columns: author, publication_year, title, journal, place_of_publication (and village_farm to associate it later to sites)
- [x] add an Extra Column called **full_reference** using {author} {publication_year}{title} {journal} {place_of_publication}
- [x] drop duplicates based on the **full_reference**
- [ ] create the [[content/Example dataset mapping/Strucke Data mapping/first draft of dataset/Entity site_references|Entity site_references]] and do the joins

````
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

`````




![[Entity biblio schema.png]]