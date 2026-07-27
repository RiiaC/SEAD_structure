---
publish: true
permalink: /Example dataset mapping/AFL Radiocarbon Data mapping/AFL Radiocarbon Data spreadsheet/E. Lab nr.md
aliases:
  - E.
---

> [!info]  The Lab nr column
> Contains a combination of letters and numbers, each of which is unique, and appears to be the sample designation used by the laboratory for analysis. Therefore, it is a good match for [[sample_name]]. However, in SEAD every sample must be part of a sample group, therefore, before entering the [[sample_name]] it is first necessary to set up the corresponding sample group information and its link back to the site from which the sample was obtained.

![[images/Radiocarbon data column E.png]]

# sample groups

- create and fill in a sheet called **sample groups** with the following columns:
- **system\_id** This column is filled incrementally, starting with 1 and is used during the import process to keep track of the data in this sheet, and to cross-reference its connections to the other sheets.
- **[[site_id]]** copy this information from the system\_id numbers of the sites sheet (even if a given site already has a SEAD site\_id). _(If it helps to keep track of which ones have been done, you can also add a column to show the corresponding **site\_name** on this sheet, but it is not needed for the import process, this column is enough to connect the information for the relational part of the database.)_
- **[[sampling_context_id]]** Fill in the appropriate number that describes the context in which the samples were collected (e.g. 1  =  Archaeological site, 2 = Other modern... 5 = Stratigraphic sequence, etc.)

> [!warning] finish filling in this page from here

- **[[method_id]]**
- **sample\_group\_name**
- **sample\_group\_description**

> [!info]  After the sample group information exists it is possible to create and link the information on the samples themselves.

# physical samples

- create and fill in a sheet called **physical samples** with the following columns:
- **system\_id** This column is filled incrementally, starting with 1 and is used during the import process to keep track of the data in this sheet, and to cross-reference its connections to the other sheets.
- [[sample_group_id]] copy this information from the **system\_id** numbers of the **sample group** sheet
- [[alt_ref_type_id]]
- [[sample_type_id]]
- [[sample_name]] This is where we copy the information from this column (**E. Lab nr**)
- [[date_sampled]] if know, add the date sampled
- [[physical_sample_id]] If any of these sample has previously been entered into SEAD due to having also been analysed as part of another data set, look up their physical\_sample\_id numbers and enter them here.
