---
table_name: tbl_site_property_type
primary_key: "[[property_type_id]]"
foreign_keys:
  - "[[site_id]]"
columns:
  - "[[property_type]]"
  - "[[property_type_description]]"
connected_tables:
  - "[[tbl_site_properties]]"
---
> [!info] This is a new table that Roger mentioned during the [2026-03-03 shape-shifter working meeting](obsidian://open?vault=UmUArkeologi_Obsidian&file=m%C3%B6ter%2FSEAD%20taskforce%20meetings%2F2026-03-03%20shape-shifter%20working%20meeting) as a nice solution for the fact that we have a variety of different types of [[national_site_identifier]] numbers, and that there are other sorts of properties that a site could have. 

Various site properties that exist in the Strucke Data that will need to be added to this table:


| property type name | property type description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| RAÄ_number         | the older form of the Swedish national site identifier number, which includes both the name of the parish and a site number. These were meant to be unique identifiers, but it turns out that some parish names exist in more than one province, which resulted in more than one site having the same RAÄ number. Therefore, the Swedish National Heritage Board assigned a unique "Lämningsnummer" for each site instead, and has phased out the introduction of new RAÅ numbers. However, as RAÄ numbers appear in the literature, it is important to keep them on file in SEAD, where they are known. Therefore, I propose that when both a Lämningsnummer and an RAÄ number are known, the Lämningsnummer be stored under [[national_site_identifier]], while the RAÄ number is a [[site_property]] |
| uppdragsnummer     | the official government number on record for a specific Swedish archaeological excavation)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| type_of_site       | the type of site (burial, settlement, Boplats, Kloster, etc.)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



