---
publish: true
permalink: /Example dataset mapping/Strucke datamapping with Brunos code/Entity superabundances.md
---

> [!info] This is an extra entity that Bruno created to make it possible two split multiple species, elements, and modification types into different rows
> The important thing here is the `abundance_key`, a unique id for everything we need to count (so for the rows with 6 species, each of them will be counted once)

This one creates a bunch of new columns, some of which are just a single step towards a later goal

# species\_1

uses `=trim(regex_extract(lower(species), '^([^,]+)', 1))` to pull the first species from a list of them in a single cell
(repeats with different code for up to `species_6`, because there are that many in one of them!)

# element name

- [ ] fill in the rest using notes at https://github.com/Br1CM/sead\_strucke\_data\_cleaning/blob/split-archive-current-pipeline/current/docs/shapeshifter\_guide.md
- \[ ]
