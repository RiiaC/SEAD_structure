---
table_name: tbl_abundance_elements
primary_key: "[[abundance_element_id]]"
foreign_keys:
  - "[[record_type_id]]"
columns:
  - "[[date_updated]]"
  - "[[element_description]]"
  - "[[element_name]]"
connected_tables:
  - "[[tbl_record_types]]"
date created: Friday, September 19th 2025, 3:37:16 pm
---
> [!warning] The [[abundance_element_id]]  foreign key can be null for both of the children tables, [[tbl_abundances]]  and [[tbl_dating_material]]. Therefore, this is an optional table. 
> - We do not appear to have any information in the [[content/Example dataset mapping/Strucke Data mapping/first draft of dataset/index|Strucke data ]] that counts as an "element" to count, so the abundance can simply be tied to species

> [!abstract] Contains reference data that defines the type of element, part, or unit being counted, as indicated by the values in tbl_abundances. 
> For insects, this is often the Minimum Number of Individuals (MNI), but it can also include individual body parts such as wings, shells, or leg segments. For plant remains (macrofossils), it generally represents specific plant parts like seeds, leaves, or bud scales.
# 1: Insects & similar (Insect and other arthropod taxa, along with other remains commonly extracted when analysing insect samples)

| abundance_element_id | record_type_id | element_name         |
| -------------------- | -------------- | -------------------- |
| 1                    | 1              | Whole arthropod      |
| 5                    | 1              | MNI                  |
| 6                    | 1              | Left elytron         |
| 7                    | 1              | Right elytron        |
| 8                    | 1              | Thorax               |
| 9                    | 1              | Head                 |
| 10                   | 1              | Body segment (other) |
| 11                   | 1              | Leg                  |
| 17                   | 1              | Aedeagus             |
# 2: Plants & pollen (Plants taxa and their pollen. Also includes non-pollen palynomorphs commonly counted and included in pollen analyses)

| abundance_element_id | record_type_id | element_name                |
| -------------------- | -------------- | --------------------------- |
| 2                    | 2              | Pollen grain                |
| 3                    | 2              | Leaf                        |
| 4                    | 2              | Seed grain                  |
| 12                   | 2              | Flower                      |
| 13                   | 2              | Leaf bud                    |
| 18                   | 2              | Needle                      |
| 19                   | 2              | Cone                        |
| 20                   | 2              | Flower bud                  |
| 21                   | 2              | Flower                      |
| 22                   | 2              | Leaf sheath                 |
| 23                   | 2              | Culm node (solid)           |
| 24                   | 2              | Culm node (hollow)          |
| 25                   | 2              | Culm node (undefined)       |
| 26                   | 2              | Ear                         |
| 27                   | 2              | Spikelet                    |
| 28                   | 2              | Chaff                       |
| 29                   | 2              | Awn fragment                |
| 30                   | 2              | Spikelet fork               |
| 31                   | 2              | Rachis fragment             |
| 32                   | 2              | Glume base                  |
| 33                   | 2              | Rachis segment(S)           |
| 34                   | 2              | Palea                       |
| 35                   | 2              | Lemma                       |
| 36                   | 2              | Glume                       |
| 37                   | 2              | Whole plant                 |
| 39                   | 2              | Shell                       |
| 40                   | 2              | Berry                       |
| 41                   | 2              | Stem                        |
| 42                   | 2              | Twig                        |
| 43                   | 2              | Bark                        |
| 44                   | 2              | Wood                        |
| 45                   | 2              | Root                        |
| 46                   | 2              | Corm (Root bulb/root tuber) |
| 47                   | 2              | Cone scale                  |
| 48                   | 2              | Endosperm                   |
| 49                   | 2              | Straw                       |
# 3: Non-pollen palynomorphs ((Fossil) remains often extracted in association with pollen analyses)  

| abundance_element_id | record_type_id | element_name |
| -------------------- | -------------- | ------------ |
| 16                   | 3              | Spore        |
| 38                   | 3              | Unknown      |

# 4: Molluscs (Snails and shellfish, terrestrial or aquatic)  

| abundance_element_id | record_type_id | element_name |
| -------------------- | -------------- | ------------ |
| 14                   | 4              | Shell        |
# 8: Cladocera  ( Water fleas, an order of the class Brachiopoda, small aquatic crustaceans, of which Daphnia is the most commonly useful genus.)    

| abundance_element_id | record_type_id | element_name |
| -------------------- | -------------- | ------------ |
| 15                   | 8              | Carapace     |

 ![[Entity abundance_element schema.png|800]]
 
| abundance_element_id | element_name                |
| -------------------- | --------------------------- |
| 2                    | Pollen grain                |
| 3                    | Leaf                        |
| 4                    | Seed grain                  |
| 12                   | Flower                      |
| 13                   | Leaf bud                    |
| 18                   | Needle                      |
| 19                   | Cone                        |
| 20                   | Flower bud                  |
| 21                   | Flower                      |
| 22                   | Leaf sheath                 |
| 23                   | Culm node (solid)           |
| 24                   | Culm node (hollow)          |
| 25                   | Culm node (undefined)       |
| 26                   | Ear                         |
| 27                   | Spikelet                    |
| 28                   | Chaff                       |
| 29                   | Awn fragment                |
| 30                   | Spikelet fork               |
| 31                   | Rachis fragment             |
| 32                   | Glume base                  |
| 33                   | Rachis segment(S)           |
| 34                   | Palea                       |
| 35                   | Lemma                       |
| 36                   | Glume                       |
| 37                   | Whole plant                 |
| 39                   | Shell                       |
| 40                   | Berry                       |
| 41                   | Stem                        |
| 42                   | Twig                        |
| 43                   | Bark                        |
| 44                   | Wood                        |
| 45                   | Root                        |
| 46                   | Corm (Root bulb/root tuber) |
| 47                   | Cone scale                  |
| 48                   | Endosperm                   |
| 49                   | Straw                       |
# 3: