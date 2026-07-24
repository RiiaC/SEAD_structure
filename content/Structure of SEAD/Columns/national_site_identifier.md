---
column_name: national_site_identifier
data_type: character varying
connected_tables:
  - "[[tbl_sites]]"
date created: Friday, September 19th 2025, 3:37:17 pm
---
A unique identifier assigned to the site by the national authority.

> [!info] to add somewhere
> Each site can have multiple national identifiers of different types. Many sites will have a Lämningsnummer and an RAÄ-nr. The RAÄ-nr must _always_ a combination of the Socken and number (so concatenate the fields on import). Each identifier should go into a separate record (not separated by a semicolon in the same field)
