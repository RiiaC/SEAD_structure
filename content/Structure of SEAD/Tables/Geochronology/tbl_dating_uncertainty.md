---
table_name: tbl_dating_uncertainty
primary_key: "[[dating_uncertainty_id]]"
columns:
  - "[[date_updated]]"
  - "[[description]]"
  - "[[uncertainty]]"
date created: Friday, September 19th 2025, 3:37:16 pm
publish: true
---

Defines various types of dating uncertainties, such as 'from', 'to', 'circa (Ca.)', and '?'. These uncertainties help specify date ranges or approximate periods, such as 'from Mesolithic to Neolithic' or 'from AD 100 to AD 300'.
 
| dating_uncertainty_id | description                                                                                                                                                                                                        |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 1                     | Indication that the date is approximate, with unspecified or unquantifiable errors.Ca.                                                                                                                             |
| 2                     | (For radiometric dates only). Oldest possible age of sample, often representing open ended dating where only one extreme limit is known. Occasionally used as part of a >< pair to define approximate age range.   |
| 3                     | (For radiometric dates only). Youngest possible age of sample, often representing open ended dating where only one extreme limit is known. Occasionally used as part of a >< pair to define approximate age range. |
| 4                     | Oldest possible age of sample, usually part of a from-to pair, but could be used to represent open ended dating.                                                                                                   |
| 5                     | Youngest possible age of sample, usually part of a from-to pair, but could be used to represent open ended dating.                                                                                                 |
| 6                     | Approximate oldest possible age of sample, usually part of a from-to pair, but could be used to represent open ended dating.                                                                                       |
| 7                     | Approximate youngest possible age of sample, usually part of a from-to pair, but could be used to represent open ended dating.                                                                                     |
| 8                     | Dating is disputable.                                                                                                                                                                                              |


