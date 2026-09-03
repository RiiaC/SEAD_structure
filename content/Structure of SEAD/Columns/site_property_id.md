---
publish: true
permalink: /Structure of SEAD/Columns/site_property_id.md
---

> [!info] This is a new column to go with the new table that Roger mentioned during the [2026-03-03 shape-shifter working meeting](obsidian://open?vault=UmUArkeologi_Obsidian\&file=m%C3%B6ter%2FSEAD%20taskforce%20meetings%2F2026-03-03%20shape-shifter%20working%20meeting) as a nice solution for the fact that we have a variety of different types of [[national_site_identifier]] numbers, and that there are other sorts of properties that a site could have.
> The table is not yet searchable in pgAdmin as of directly after that meeting, but he says that he has given it to Johan to deploy. Therefore, the above are only my guesses as to what the table might be called, and what columns might wind up in the table
> later that day Roger sent:
>
> I gave you wrong tables names. These to selects works on out staging server. Bort tables are new and empty.
> select \*
> from tbl\_site\_properties
>
> select \*
> from tbl\_property\_types
