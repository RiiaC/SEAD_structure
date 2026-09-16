---
publish: true
permalink: /Example dataset mapping/Strucke datamapping with Brunos code/Entity supergeochron.md
---

> [!info] This is an extra entity that Bruno created to make it possible to extract the lab names from the lab\_id number and to make the connection to the geochronrefs table easier.
>
> Note that since Bruno created this, we noticed  that some rows have more than one lab\_id number in the same cell, so it will need another step to extract those

This one creates a bunch of new columns, some of which are just a single step towards a later goal

# lab\_id\_stripped

This one removes "Okänd" from the dataset (because if we don't know the lab number, then it should be null, and because some of the official lab codes happen to use letter pairs that occur in the name "Okänd", and not doing this step would result in assigning that lab, which would be wrong)

# lab\_id\_prefix\_leading

- fill in the explanations for this, and the rest from https://github.com/Br1CM/sead\_strucke\_data\_cleaning/blob/split-archive-current-pipeline/current/docs/shapeshifter\_mappings/lab\_prefix\_replacements.yml
-
