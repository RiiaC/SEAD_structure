---
publish: true
---
![[SEAD logo.png]]
The below tables show various categories of information that can be imported into SEAD. Some of these lists have been extracted from templates developed at [Umeå Environmental Archaeology Laboratory, MAL](https://www.umu.se/en/research/infrastructure/mal/) for some of their standard data types to be imported into SEAD. Excel versions of these template files are available on request.

For all of the below tables, the required data is in **bold print**, optional data is in regular print. Note: the below table and column descriptions are modified from the corresponding descriptions on https://humlab-sead.github.io/sead-schema/index.html unless otherwise specified.

# Site
All data in SEAD must be associated with a specific named site, with a recorded latitude and longitude. It is possible to record additional information about the site and location, including:

| Column name     | Description                                                                                                                                   |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **Site name**   | **Primary name of the archaeological site, as used in project documentation or cultural heritage registers.**                                 |
| Settlement      | Name or designation of the settlement to which the site belongs, or an indicator that the site represents a settlement context.               |
| RAÄ Number      | Identifier assigned to the site by the Swedish National Heritage Board (Riksantikvarieämbetet, RAÄ), used for national heritage registration. |
| Lämningsnummer  | Official heritage register number identifying the individual monument or archaeological remain within the RAÄ system.                         |
| **Latitude**    | **Geographic latitude of the site location, expressed in decimal degrees.**                                                                   |
| **Longitude**   | **Geographic longitude of the site location, expressed in decimal degrees.**                                                                  |
| Altitude        | Elevation of the site above sea level, expressed in metres.                                                                                   |
| Landskap        | Historical province (landskap) in which the site is located.                                                                                  |
| Län             | Swedish county (län) in which the site is located.                                                                                            |
| Fylke           | Norwegian county (fylke), if applicable for sites located in Norway.                                                                          |
| Socken          | Historical parish (socken) associated with the site.                                                                                          |
| Kommun          | Current municipality (kommun) in which the site is located.                                                                                   |
| Koordinatsystem | Coordinate reference system used for spatial data (e.g. SWEREF 99 TM, WGS84).                                                                 |
# Features
When samples are associated with a specific archaeological feature that information can be recorded in SEAD:

| Column name  | Description                                                                                                                                                                |
| ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Feature Name | Name or identifier assigned to the archaeological feature, as used in field documentation or project records.                                                              |
| Feature Type | Classification of the feature based on form or function (e.g. hearth, pit, posthole, ditch), following project or standard archaeological terminology.                     |
| Description  | Free‑text description of the feature, summarising observed characteristics such as morphology, composition, dimensions, stratigraphic relationships, and notable contents. |
# Sample Group
The sample group is a required category for SEAD because it is the level to which many of the other tables are attached. It contains collections of related samples, typically grouped by structures (e.g., House 1), stratigraphic sequences (e.g., profile 3), or lake cores. It could also refer to a collection of bones from a single skeleton. Groups can be defined flexibly based on research needs. In the case of isolated single samples, they still need to be assigned to a sample group, but in those cases the group contains only one sample.

| Column name              | Description                                                                                                                                                                                                                                                                                                                                                                           |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Sample group name**    | **A unique identifier name for the sample group. (For ceramics, this should be the vessel number.)**                                                                                                                                                                                                                                                                                  |
| Sample group description | A definition or description of groups of samples, categorized by a specific description type.                                                                                                                                                                                                                                                                                         |
| Type                     | This table categorizes the types of descriptions related to sample groups. It includes types such as architectural data (e.g., roof type, structural details) or dendrochronological anlabels related to shipwrecks. Note that these descriptions are intended to provide context and should not be used to infer specific features of the samples. Users can add custom lookup data. |
| Publication              | Contains bibliographic information specifically relevant to a sample group, distinct from site or dataset references (e.g., a publication that reinterprets a structure within a site).                                                                                                                                                                                               |

# Physical Samples
This table records information about physical samples collected from specific sites. Each sample is characterised by its location within the site, its physical properties measured in specific units (e.g., liters, kilograms), and its context within its sample group. Additionally, samples may have descriptive information, notes, and external identifiers linked to other systems.

| Column name         | Description                                                                                                                                                                                                                                            |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| sample name         | Primary reference number or name of the sample. Additional references can be recorded as alternative names.                                                                                                                                            |
| Alternative names   | Other names or identifiers used for the sample in field records, legacy datasets, or publications.                                                                                                                                                     |
| Feature             | Archaeological feature from which the sample was taken (e.g. hearth, pit, layer), as defined in site documentation.  Note: A sample may derive from multiple features (e.g., ‘c107’ within ‘well 47’), but each feature should be recorded separately. |
| Synonyms            | Additional identifiers or alternative labels referring to the same sample or sampling context.                                                                                                                                                         |
| Sample type         | Material type of the sample (e.g. sediment, soil, charcoal, bone), describing its physical composition.                                                                                                                                                |
| Sample method       | Method by which the sample was collected (e.g. bulk sample, column sample, spot sample), describing the sampling strategy.                                                                                                                             |
| Sample Group        | Name of the SEAD sample group to which the sample belongs, linking it to a defined conceptual or analytical grouping.                                                                                                                                  |
| X (N)               | Northing (X) coordinate of the sample location, expressed in the coordinate system specified for the site.                                                                                                                                             |
| Y (E)               | Easting (Y) coordinate of the sample location, expressed in the coordinate system specified for the site.                                                                                                                                              |
| Z                   | Vertical coordinate or elevation of the sample location, expressed in metres.                                                                                                                                                                          |
| Horizon             | Stratigraphic horizon, layer, or context from which the sample was taken.                                                                                                                                                                              |
| Volume before float | Volume of the sample prior to flotation, expressed in litres.                                                                                                                                                                                          |
| Volume after float  | Volume of the sample remaining after flotation, expressed in litres.                                                                                                                                                                                   |
| Sample note         | Free‑text notes providing additional information about the sample, such as preservation, deviations from standard procedures, or contextual observations.                                                                                              |
# Work progress
| Column name | Description |
| ----------- | ----------- |
| Status      |             |
| Subsample   |             |
| Floterat    |             |
| Sållat      |             |
| CitP        |             |
| CitPOI      |             |
| MS          |             |
| MS550       |             |
| LOI         |             |
# Publication
| Column name | Description                                                                                                               |
| ----------- | ------------------------------------------------------------------------------------------------------------------------- |
| Publication | The full citation information for publications relevant to a full dataset, method, sample, or other aspect of the dataset |
| Authors     | The authors of the paper                                                                                                  |
| Year        | The publication year                                                                                                      |

# Soil Chemistry: Geochemical, Physical, and Sediment Properties
This section documents laboratory measurements of sediment and soil properties, including phosphorus fractions, magnetic susceptibility, loss‑on‑ignition, pH, electrical conductivity, and grain size distribution. Together, these variables characterise the chemical composition, physical structure, and depositional or anthropogenic influences affecting the sampled material.

| Column name            | Description                                                                                                                                                                 |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Sample name            | Unique identifier for the sample, as defined by the submitting project or laboratory. Used to link analytical results to spatial, stratigraphic, or contextual information. |
| Pº weight (g)          | Dry weight of the subsample used for oxalate‑extractable phosphorus (Pº) analysis, measured in grams.                                                                       |
| Abs. Pº                | Measured spectrophotometric absorbance for oxalate‑extractable phosphorus prior to conversion to concentration                                                              |
| Pº                     | Calculated concentration of oxalate‑extractable phosphorus based on absorbance and calibration curve.                                                                       |
| Pº corr                | Oxalate‑extractable phosphorus concentration corrected for blanks, dilution, and/or sample dry weight, according to laboratory protocol.                                    |
| Ptot weight (g)        | Dry weight of the subsample used for total phosphorus (Ptot) analysis, measured in grams.                                                                                   |
| Abs.Ptot               | Measured spectrophotometric absorbance for total phosphorus prior to conversion to concentration.                                                                           |
| Ptot                   | Measured spectrophotometric absorbance for total phosphorus prior to conversion to concentration.                                                                           |
| Ptot corr              | Total phosphorus concentration corrected for blanks, dilution, and/or sample dry weight, according to laboratory protocol.                                                  |
| MS weight              | Dry weight of the subsample used for magnetic susceptibility measurement.                                                                                                   |
| MS                     | Measured mass‑specific magnetic susceptibility of the sample.                                                                                                               |
| MS corr                | Magnetic susceptibility value corrected for sample mass and/or instrument background.                                                                                       |
| MS550 weight (g)       | Weight of the subsample after ignition at 550 °C, used for post‑LOI magnetic susceptibility measurement.                                                                    |
| MS550                  | Magnetic susceptibility measured after loss‑on‑ignition at 550 °C.                                                                                                          |
| MS550 corr             | Post‑LOI magnetic susceptibility corrected for sample mass and/or instrument background.                                                                                    |
| C                      | Estimated organic carbon content derived from loss‑on‑ignition data, expressed according to laboratory calculation protocol.                                                |
| C+S                    | Combined carbon and sulphur fraction estimated from high‑temperature loss‑on‑ignition.                                                                                      |
| C+S(LOI)               | Carbon and sulphur content calculated directly from LOI mass loss values.                                                                                                   |
| LOI% (550º)            | Percentage mass loss after ignition at 550 °C, interpreted primarily as organic matter content.                                                                             |
| pH (H2O)               | Soil/sediment pH measured in a water suspension.                                                                                                                            |
| pH (KCl 0,1M)          | Soil/sediment pH measured in 0.1 M potassium chloride (KCl), reflecting exchangeable acidity.                                                                               |
| µS (H2O)               | Electrical conductivity of the soil/sediment measured in water, expressed in microsiemens (µS), indicating soluble ion concentration.                                       |
| Grain size >2mm (g)    | Mass of the coarse fraction (>2 mm), measured in grams.                                                                                                                     |
| Grain size >2mm (%)    | Percentage of the total sample mass represented by the >2 mm fraction.                                                                                                      |
| Grain size 0,6-2mm (g) | Mass of the medium sand to gravel fraction (0.6–2 mm), measured in grams.                                                                                                   |
| Grain size 0,6-2mm (%) | Percentage of the total sample mass represented by the 0.6–2 mm fraction.                                                                                                   |
| Grain size <0,6 mm (g) | Mass of the fine fraction (<0.6 mm), measured in grams.                                                                                                                     |
| Grain size <0,6 mm (%) | Percentage of the total sample mass represented by the <0.6 mm fraction.                                                                                                    |
Note: The above introduction and column descriptions written by the CoPilot AI 2026-04-27. The column descriptions from the prompt: *"I was given a spreadsheet template from the Umeå Environmental Archaeology Laboratory, MAL. They did not provide metadata descriptions of the columns. Below is the list of column names. Do you have enough information to write me good, concise, yet informative metadata descriptions for each of these?"* ==I am awaiting human conformation and/or edits to this information from the MAL staff.==
# Archaeobotany: Taxonomic and Anatomical Identification (Faunal Remains)
This section records taxonomic and anatomical identifications of faunal remains, including genus-, species-, and subspecies‑level determinations, along with uncertainty qualifiers. It also documents observed modifications and anatomical elements, providing information relevant to species representation, taphonomy, and human or natural processes affecting the remains.

|columnn name|description|
|---|---|
|Genus uncertainty|Indicator describing uncertainty or qualification associated with the genus‑level identification (e.g. cf., aff., ?, probable), as defined by laboratory or project conventions.|
|Genus|Genus to which the specimen is assigned, based on morphological identification.|
|Species uncertainty|Indicator describing uncertainty or qualification associated with the species‑level identification (e.g. cf., aff., ?, probable), as defined by laboratory or project conventions.|
|Species|Species epithet assigned to the specimen, where identification beyond genus is possible.|
|Subspecies|Subspecies designation, where applicable and identifiable, following standard zoological nomenclature.|
|Modifications|Observed modifications to the specimen indicating natural or anthropogenic alteration, such as cut marks, burning, gnawing, weathering, fragmentation, or other taphonomic features.|
|Element|Anatomical element represented by the specimen (e.g. femur, humerus, mandible, vertebra, scale), following zooarchaeological anatomical terminology.|
Note:  The above introduction and column descriptions written by the CoPilot AI 2026-04-27. The column descriptions from the prompt: _"In the same spreadsheet template from the Umeå Environmental Archaeology Laboratory, MAL another sheet has the below list of column names. Do you have enough information to write me good, concise, yet informative metadata descriptions for each of these?"_ ==I am awaiting human conformation and/or edits to this information from the MAL staff.==
# Other Macro remains by type (Charcoal, Bone, Ceramics, and Other Materials)
This section documents the presence or quantity of selected macroscopic remains recovered from samples, including charcoal, bone, ceramics, and other visible materials. These data capture coarse archaeological and environmental evidence obtained through visual sorting and provide contextual information on site formation and material deposition.

|columnn name|description|
|---|---|
|MAL nr|Unique laboratory number assigned by the Umeå Environmental Archaeology Laboratory (MAL) to the sample or analytical unit.|
|Träkol|Recorded quantity or presence of charcoal (wood charcoal) macro‑remains identified in the sample.|
|Ben|Recorded quantity or presence of bone macro‑remains identified in the sample.|
|Keramik|Recorded quantity or presence of ceramic (pottery) fragments identified in the sample.|
|Annat|Recorded quantity or presence of other macro‑remains not covered by the predefined categories (e.g. slag, shell, daub, unidentified material), as defined by the analyst.|
Note:  The above introduction and column descriptions written by the CoPilot AI 2026-04-27. The column descriptions from the prompt: _"In the same spreadsheet template from the Umeå Environmental Archaeology Laboratory, MAL another sheet has the below list of column names. Do you have enough information to write me good, concise, yet informative metadata descriptions for each of these?"_ ==I am awaiting human conformation and/or edits to this information from the MAL staff.==