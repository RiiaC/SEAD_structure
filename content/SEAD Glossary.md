---
date created: Tuesday, December 23rd 2025, 7:48:31 am
---
>[!info]+ This glossary was prepared in September 2025 
>by compiling the description information for tables exported from the SEAD database and supplementing that information with definitions of some of the terms used in those definitions. If you feel that any of these definitions need further clarification please send an [email to me](mailto:Riia.Chmielowski@umu.se).

(*Note that at this time there are no links back to the tables themselves in this glossary. This is because I have not yet learned how to exclude links to a specific note from the Graph View, and if everything links to a single note, the graph just looks like a puff ball and loses its usefulness*.)


|Term|relavant SEAD table (if any)|Definition|
| --- | --- | --- |
|Abundance|tbl_abundances|The individual count, presence, or scaled values for the biological proxies|
|Activity type|tbl_activity_types|Describes forms of activities for organisms, such as breeding, adults active, flowering etc. In terms ofmonths or seasons|
|Alternative Reference Type|tbl_alt_ref_types|The source/meaning of the alternative sample name, for example a lab number, museum number, field sample number,or on-site excavation number|
|Analysis entities|tbl_analysis_entities|The various types of analysis that have been applied to a given sample|
|Analysis entity age|tbl_analysis_entity_ages|The single proxy age determined by a specific type of analysis|
|Biblio|tbl_biblio|The bibliographic information for a given cited reference|
|Biological proxies|-|The remains of various organisms used as a basis for quantitative inferences about past climatic conditions|
|Chronology|tbl_chronologies|A cohesive collection of dated samples defined for a specific purpose, such as giving a single age rangeto each sample in a master dataset, or an age-depth model for a lake|
|Colour|tbl_colours|Name and definition of colours according to specified method or colour space (e.g.Munsell, 2.5YR)|
|Contact|tbl_contacts|An individual or organisation and their contact information (e.g. Laboratory, sample taker,dataset creator)|
|Data type|tbl_data_types|Type of quantification used for the dataset, including classification system definitions.|
|Data type groups|data_type_group_name|Grouping of different data types (e.g. Relative scale, semi-quantitative)|
|Dataset|dataset_name|A collection of analysis entities undertaken in a manner meaningful for a given proxy.|
|Dataset Masters|tbl_dataset_masters|Major grouping unit for datasets, usually designating contributing database,project, user or lab e.g. Bugscep, MAL, Lund Dendro lab|
|Dataset submissions|tbl_dataset_submisssion|Records details for different submission events for a dataset (e.g. Originalrecording to paper, entry into Bugs database, ingestion into SEAD).|
|Dating Labs|tbl_dating_labs|The official radiocarbon laboratory identifiers and names as taken fromhttp://www.radiocarbon.org/Info/labcodes.html, for transparency in C14 and other dating records|
|Dendro Dates|tbl_dendro_dates|Dendrochronological dates (calculated felling year)|
|Ecocode|tbl_ecocodes|An ecological, habitat, or ethnographic (etc.) Category to which a taxon can be assigned|
|Ecocode system|tbl_ecocode_systems|A system for classifying different aspects of taxa, such as habitat preference, foodtype, cultural use etc.|
|Element|element_name|A relevant portion of your sample proxy, such as a seed, leaf, or bud scale.|
|Feature|tbl_features|A non-portable trace of past human activity, distinct from movable artifacts, such asbuilding remains, hearths, burials, pits, roads, agricultural modifications like terraces, and defensive constructions like mounds and ditches.|
|Feature type|tbl_feature_types|Categories of features by their purpose, shape, or construction, such as domestic andpublic and ceremonial spaces, economic/industrial areas, defensive structures etc.|
|Geochron|tbl_geochronology|Pertaining to geochronology|
|Horizon|tbl_horizons|Technical name of the layer of soil a sample is taken from according to a defined standard (e.g. FAO A horizon)|
|Identification Levels|tbl_identification_levels|Look-up data for taxonomic resolution/uncertainty in identification, andtaxonomic level of uncertainty e.g. C.f. Family, c.f. Genus, c.f. Species.|
|Language|tbl_languages|Which human language was used for the common name of taxa|
|Lithology|tbl_lithology|Description of the sediment units within a sample group, which allows for a soil profileto be describedat depths in parallel to the sample depths (e.g. 0-10 cm humus, 10-30 cm sand)|
|Location types|tbl_location_types|Definitions of the resolution of geographical terms as well as their context (e.g.administrative unit, historical administrative unit, lake, country)|
|Locations|tbl_locations|Geographical location in physical (but sometimes historical) space, usually defined in terms of regions|
|MCR Birm Beetle Data|tbl_mcrdata_birmbeetledat|Definition of species climate envelopes in binary 1-degree Celsius cellsfor trange (columns) and tmax (rows);see www.bugscep.com for more info.|
|MCR Data|mcr_data|Data related to the Mean Climate Range (MCR) for each species.|
|MCR name|tbl_mcr_names|The original taxon names used in the Birmingham Mean Climate Range (MCR) calculation system forclimate reconstruction; storedto enable reproducibility and cross-comparison with older results|
|MCR number|mcr_number|A unique identifier related to each Mean Climate Range (MCR) taxon name.|
|MCR summary data|tbl_mcr_summary_data|Simple summaries of the maximum extent of the temperature tolerance of Mean Climate Range (MCR) species|
|Measured Value Dimension|tbl_measured_value_dimensions|Actual amount of the measured values, for example the weight ofsamples used in measured value table, preandpost burning weights, or the volume or other dimension measures.|
|Measured Values|measured_value|A continues (non-discrete) chemical or physical (non-taxa) value of a certaindimension; a Sample Analysis canhave (zero or) one measured value|
|Measurement|measurement|The specific coordinate measurement value.|
|Measurement Value|measurement_value|Numeric value representing the measurement obtained from the ceramic analysis.|
|Method|tbl_methods|Definition of the analysis methods used|
|Method Groups|tbl_method_groups|Groups of analysis methods that have some form of similarity (e.g. Datingmethods, isotope analyses, palaeoentomology, geographical location)|
|Minium Number of Individuals|-|The minimum number of whole individuals (MNI) of a given speciesneeded to account for the assemblage of insectbodyparts present in a sample for that species|
|Modifications|tbl_modification_types|A naturally occuring alteration to the original sample material during or after deposition (but before collection), for example carbonised, corroded, or calcified|
|National grid|tbl_site_natgridrefs|The general site coordinates using national grid system, e.g. UK Ordinance surveynational Grid, swedishsweref99. A site can be defined on multiple grids (e.g. Swedish RT90 and SWEREF99TM)|
|Physical Samples|tbl_physical_samples|Physical samples represent a sampling unit from which analyses are extracted;for example, with soil samples,these represent a lump of sediment, from which various analyses can be extracted (e.g. Pollen, insects etc).|
|Project|tbl_projects|Name and description of the project context of datasets for site(s); now a form of metadata|
|Project Stages|tbl_project_stages|Stages of investigation e.g. Desktop study, prospection, full excavation, reanalysis|
|Project Types|tbl_project_types|Describes the type of investigation in terms of main purpose/aim, e.g. Teaching,consultancy, research, or combinations of these|
|Radiocarbon Calibration|-|An in-database tool/approximate calibration curve for rapid calculationof age-depth curves and equivalent agepreviews prior to applying full and accurate probability density function based calibrated ages (based on Neotoma htpp://www.neotomadb.org)|
|Rarity data (RDB)|tbl_rdb|Rarity data for a taxon for a specified geographical area (e.g. Threatened in Sweden)|
|RDB System|rdb_system|Description of rarity designation systems (so called red data books) and the regionfor which they are applicable|
|Record Types|tbl_record_types|Used to group biological proxies according to the way they are generally used,and/or their origin. It isusedto provide useful subsets of the full taxonomic index abundance elements (i.e. So that "seed" is not an available option for insect data) and methods. Groups are made at the "Order" level in the taxonomic tree. E.g. "Insects & similar" groups insects with arthropods and other animals commonly extracted during insect work. "Plants & pollen" are grouped as they have similar ecological implications (i.e. Presence of plant).|
|Relative Ages|tbl_relative_ages|Both period and calendar (single or year range) chronological definitions. Perioddefinitions are storedonlyonce per geographical occurrence (e.g. Germany and Sweden can have different Bronze Age definitions) and assigned to samples through the relative dates table.|
|Relative dates|tbl_relative_dates|Specific instances of relative ages (calendar or period based) assigned to a physicalsample; also indicates the method used to associate sample with date (e.g. Stratigraphic dating, typological association)|
|Sample Dimensions|tbl_sample_dimensions|Measurable dimension type data for samples, excluding coordinates, butincluding depth or sample in stratigraphy or core; for example, the size of sample on arrival (volume, weight etc), depth of sample top, depth of sample bottom|
|Sample Group Sampling Contexts|tbl_sample_group_sampling_contexts|The type of situation under which the sample group wascollected, investigation purpose, or other initialcollection purpose (e.g. Stratigraphic sequence, invertebrate survey, archaeological excavation, quantitative vegetation survey); it provides a collection context for the sample group and provides for extraction/analysis on only samples collected in a specific type of project. For example, climate reconstruction using only stratigraphic sequences, habitat analysis using only modern survey data.|
|Sample Groups|tbl_sample_groups|A collection of related samples, such as all samples from a specific structure (e.g.house 1), a stratigraphicsequence (e.g. Profile 3) or a lake core|
|Sample Types|tbl_sample_types|The physical form of the sample, usually either subsamples relating the samplegroup sampling method, orbulksamples (e.g. Core subsample, grab sample, bulk (bag) sample)|
|Sampling context|sampling_context|Concise and descriptive name for the sampling context, e.g., stratigraphic sequence or archaeological excavation.|
|Site|tbl_sites|A single Location excavated or sampled for the purpose of building environmental pre- andhistorical datarecords|
|Site preservation status|tbl_site_preservation_status|Information on preservation level of sites and risks to cultural heritage|
|Species Associations|tbl_species_associations|The relationship of one taxon to others, such as predation, parasitism,common habitat etc.; also includes synonym links. Note that the direction of the association is important in most cases (e.g. X predates on y)|
|Submission Type|submission_type|The type of dataset submission, such as original submission or ingestion fromanother database|
|Taxa Synonyms|tbl_taxa_synonyms|Alternative scientific names of taxa, including primary reference for definitionor use.|
|Dimensions|tbl_dimensions|The name and description of the different measurement types, such as sampleweight, core length, according toa method group.|
|Text, Biology|biology_text|descriptive information about the ecological, habitat and behavioural information for taxa (e.g. In hollowson old oaks)|
|Text, Distribution|tbl_text_distribution|Descriptive information for taxa, including reference for the source (e.g. Scandinavia northof Tromsø, British Isles– rare)|
|Units|tbl_units|Measurement unit definitions (e.g. Mm, millimetres)|
|Years Types|tbl_years_types|Contains the names and descriptions of different types of years used for dating, such as radiocarbon or calendar years.|