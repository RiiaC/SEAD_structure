---
table_name: tbl_value_classes
primary_key: "[[value_class_id]]"
foreign_keys:
  - "[[method_id]]"
  - "[[parent_id]]"
  - "[[value_type_id]]"
columns:
  - "[[source/docs/plugins/Description]]"
  - "[[name]]"
  - "[[value_class_uuid]]"
connected_tables:
  - "[[tbl_methods]]"
  - "[[tbl_value_classes]]"
  - "[[tbl_value_types]]"
publish: true
---

Specifies a value class describing e.g. a data column

# Dendrochronology value classes
 
| [[value_class_id]] | [[value_type_id]] | [[parent_id]] | name                            | description                                                                                                                                    |
| ------------------ | ----------------- | ------------- | ------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| 1                  | 8                 | NULL          | Tree species                    | Species name of the tree the sample came from.                                                                                                 |
| 2                  | 1                 | NULL          | Tree rings                      | Number of measured tree rings inferred as years.                                                                                               |
| 3                  | 12                | NULL          | Earlywood/Latewood              | A notation in case the outermost ring is not complete. +ew in case only earlywood is present, -lw in case some part of the latewood is missing |
| 4                  | 1                 | NULL          | Number of analysed radii.       | Number of analysed radii.                                                                                                                      |
| 5                  | 3                 | NULL          | EW/LW measurements              | Record of whether the earlywood and latewood of each ring has been measured separately.                                                        |
| 6                  | 1                 | NULL          | Sapwood (Sp)                    | Number of sapwood rings, which is the outer layers of a tree, between the heartwood and cambium.                                               |
| 7                  | 3                 | NULL          | Bark (B)                        | Whether bark was present in the sample.                                                                                                        |
| 8                  | 13                | NULL          | Waney edge (W)                  | The last formed tree ring before felling or sampling. Presence of this represents the last year of growth.                                     |
| 9                  | 1                 | NULL          | Pith (P)                        | Number of rings missing between the core of the tree and the first measured ring.                                                              |
| 10                 | 5                 | NULL          | Tree age ≥                      | The analysed age of the tree.                                                                                                                  |
| 11                 | 5                 | NULL          | Tree age ≤                      | The analysed age of the tree.                                                                                                                  |
| 12                 | 6                 | NULL          | Inferred growth year ≥          | The growth year inferred from the analysed tree rings.                                                                                         |
| 13                 | 6                 | NULL          | Inferred growth year ≤          | The growth year inferred from the analysed tree rings.                                                                                         |
| 14                 | 10                | NULL          | Estimated felling year          | The felling year as inferred from the analysed outermost tree-ring date                                                                        |
| 15                 | 10                | NULL          | Possible estimated felling year | Used for samples where dating has not been succesful but a non-statistically satisfactory dating suggestion is given.                          |
| 16                 | 7                 | NULL          | Provenance                      | The provenance of the sampled tree, inferred by comparing the sample with others.                                                              |
| 17                 | 10                | NULL          | Outermost tree-ring date        | The date of the outermost tree-ring                                                                                                            |
| 18                 | 3                 | NULL          | Not dated                       | Used to mark samples as not having been succesfully dated, i. e. analysed but not dated                                                        |
| 19                 | 7                 | NULL          | Date note                       | Notes on  a sample.                                                                                                                            |
| 20                 | 7                 | NULL          | Provenance comment              | Comments on the provenance of a sample                                                                                                         |
| 21                 | 1                 | NULL          | Non-measured tree rings         | Estimated number of non-measured tree rings outside the outermost measured tree ring.                                                          |
| 22                 | 1                 | NULL          | Non-measured sapwood rings      | Estimated number of non-measured sapwood rings outside the outermost measured tree ring1                                                       |
| 24                 | 10                | NULL          | Innermost tree-ring date        | The date of the innermost tree-ring                                                                                                            |
| 23                 | 1                 | 6             | Sapwood indicator               | Indicates if sample has sapwood, which is the outer layers of a tree, between the heartwood and cambium.                                       |

# Ancient DNA analysis value classes

|value_class_id|value_type_id|parent_id|name|description|
|---|---|---|---|---|
|43|17|NULL|Molecular sex - Rx|Prediction of molecular sex of individual. Rx is based on the ratio of reads aligning to the X chromosome and autosomes.|
|42|9|NULL|mtDNA haplogroup|Prediction of mitochondrial DNA haplogroup.|
|41|9|NULL|Y haplogroup|Prediction of Y chromosome haplogroup.|
|40|9|NULL|1st deg. relatives|List of sample IDs that are 1st degree relatives to the analysed individual.|
|39|9|NULL|2nd deg. relatives|List of sample IDs that are 2nd degree relatives to the analysed individual.|
|38|9|NULL|>2nd deg. relatives|List of sample IDs that are further than 2nd degree relatives to the analysed individual.|
|37|14|NULL|Library preparation(s)|Type of sequence library preparation (e.g. blunt-end, single-stranded, etc.).|
|36|16|NULL|Damage treatment(s)|Type of damage treatment if applicable (e.g. UDG).|
|35|15|NULL|SNP capture|Type of SNP capture if applicable (e.g. 1240k).|
|34|7|NULL|Metagenomics analysis|Record of whether the library been subjected to a metagenomic analysis.|
|54|9|NULL|Organism genome mapped to|Organism whose reference sequence / genome assembly was used for sequence alignment.|
|53|9|NULL|Reference genome assembly|reference sequence / genome assembly name or accession code.|
|52|1|NULL|Endogenous reads (filtered)|The number of sequence reads which have successfully mapped to the organism reference sequence after filtering.|
|51|11|NULL|Average read length|The average length of mapped sequence reads, excluding reads shorter than 35 bases and reads with less than 90% consensus to the species reference.|
|50|11|NULL|Average depth of coverage - genome (x)|The number of times on average that a given nucleotide in the genome has been sequenced.|
|49|4|NULL|Breadth of coverage - genome (%)|The percentage of the reference sequence / genome assembly covered after alignment.|
|48|11|NULL|Average depth of coverage - mtDNA (x)|The number of times on average that a given nucleotide in the mitochondrial genome has been sequenced.|
|47|2|NULL|mtDNA reads|The number of sequence reads which have successfully mapped to the mitochondrial DNA in the reference sequence.|
|46|2|NULL|X chromosome reads|The number of sequence reads which have successfully mapped to the X chromosome in the reference sequence.|
|45|1|NULL|Y chromosome reads|The number of sequence reads which have successfully mapped to the Y chromosome in reference sequence.|
|44|17|NULL|Molecular sex - Ry|Prediction of molecular sex of individual. Ry is based on the ratio of reads aligning to the X and Y chromosomes.|
|33|9|NULL|General library file name|General file name suffix for library DNA sequence fastq files, BAM files, etc.|
|32|1|NULL|Merged reads|The total number of merged sequence reads retained following adapter removal and merging of read pairs.|
|31|2|NULL|Endogenous reads (raw)|The number of sequence reads which have successfully mapped to the organism reference sequence before filtering.|
|30|4|NULL|Raw endogenous content (%)|The number of sequence reads which have successfully mapped to the organism reference sequence after filtering.|
|29|4|NULL|Duplicate reads (%)|The percentage of mapped sequence reads that are PCR duplicates i.e. they have identical start and end positions.|
|28|4|NULL|Short reads (%)|The percentage of mapped sequence reads that are shorter than 35 bases.|
|27|11|NULL|5’ damage|Proportion of T nucleotides (given C nucleotide in reference) at the 5’ end of sequence reads. Representative of damage to DNA due to deamination of cytosines.|
|26|11|NULL|3’ damage|Proportion of A nucleotides (given G nucleotide in reference) at the 3’ end of sequence reads. Representative of damage to DNA due to deamination of cytosines on complementary strand.|
|25|7|NULL|Methods metadata download link|Link to methods metadata worksheet (with lab and bioinformatics methods, tools, parameters, etc.).|

