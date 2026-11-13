---
publish: true
permalink: /Structure of SEAD/Tables/Abundance Domain/tbl_property_type.md
created: 2026-07-24T09:34:41.275Z
modified: 2026-11-13T14:25:50.907Z
published: 2026-11-13T14:25:50.907Z
table_name: tbl_site_property_type
primary_key: "[[property_type_id]]"
columns:
  - "[[property_type_description]]"
  - "[[property_type]]"
connected_tables:
  - "[[tbl_site_properties]]"
foreign_keys:
  - "[[site_id]]"
required: No
role: classifier
domain:
  - abundance
  - spatial
---

> [!info] Shared property-type vocabulary used by SEAD property tables.
> Property types can exist under both the [Abundance Domain](obsidian://open?vault=SEAD_structure_Obsidian\&file=Structure%20of%20SEAD%2FTables%2FAbundance%20Domain%2Findex), and the [Spatial Domain](obsidian://open?vault=SEAD_structure_Obsidian\&file=Structure%20of%20SEAD%2FTables%2FSpatial%20Domain%2Findex).

For the Strucke Data, this table is a nice solution for the fact that we have a variety of different types of [[national_site_identifier]] numbers, specifically:

| property type name | property type description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| RAÄ\_number         | the older form of the Swedish national site identifier number, which includes both the name of the parish and a site number. These were meant to be unique identifiers, but it turns out that some parish names exist in more than one province, which resulted in more than one site having the same RAÄ number. Therefore, the Swedish National Heritage Board assigned a unique "Lämningsnummer" for each site instead, and has phased out the introduction of new RAÅ numbers. However, as RAÄ numbers appear in the literature, it is important to keep them on file in SEAD, where they are known. Therefore, I propose that when both a Lämningsnummer and an RAÄ number are known, the Lämningsnummer be stored under [[national_site_identifier]], while the RAÄ number is a [[site_property]] |
| uppdragsnummer     | the official government number on record for a specific Swedish archaeological excavation)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| type\_of\_site       | the type of site (burial, settlement, Boplats, Kloster, etc.)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
