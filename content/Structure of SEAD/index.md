---
publish: true
permalink: /Structure of SEAD/index.md
---

# Welcome to an illustration of SEAD's Database Structure

> [!info] The Strategic Environmental Archaeology Database (SEAD)
> is a national research infrastructure for environmental archaeology data developed and managed at the Environmental Archaeology Lab (MAL) in collaboration with Humlab at Umeå University, Sweden. For more information, check out the [SEAD web page](https://www.sead.se/), or check out the [SEAD Browser](https://browser.sead.se/) to explore the data itself.

This section of the web page provides a graphical representation of the structure of the SEAD database, with a page for every table and column in the database itself with links showing which columns are part of what tables. This representation of SEAD's structure is intended to be a compliment to the [official public record for the SEAD database schema.](https://humlab-sead.github.io/sead-schema/) by providing an easily link-able version of the structure for the [[Example dataset mapping/AFL Radiocarbon Data mapping/index|example data mapping]] provided in the other section of this web page.

> [!tip] One can explore the database structure either through the web page menu, or by clicking on the upper right corner of the graphical interface to expand the graph.
> On mobile devices it takes a bit of time to open the graph, but once open, it works.

> [!warning]  Graph View
> The graph view in the web version currently shows all of the connections between all of the files, and thus can be a bit overwhelming. The Obsidian version of this vault lets one filter to a subset of the data. I may someday try to add that feature to the web version.

> [!abstract]+ Canvas
> The Canvas plugin permits diagram maps showing connections between the various tables. My [[first draft SEAD Structure.canvas]] started a traditional database mapping approach, wherein each table appears only once, and connections are drawn between all connected tables. However, well before I had done more than a small sub-set of these I could see that this would be too messy.
> Therefore, instead, I have started a newer [[SEAD Structure.canvas]] file that groups tables into clusters of tables that connect to a single, central table. Connection lines between groups (rather than the individual tables) are also drawn.  With this approach some tables appear in multiple groups. Where this is the case, each copy of the same table shares the same colour, making it easy to spot the connecting table(s) in two connected groups.

![[SEAD Structure.canvas]]
this is very much a work in progress, and not all aspects of the Canvas documents in the Obsidian vault translate correctly in the web version (and not all of the connections for the major groups have been mapped, yet.

If you have any questions, you may contact me directly.

\--[Riia ](https://www.umu.se/en/staff/riia-chmielowski/), SEAD Project Assistant/Data Steward
2026-07-21

_This illustration of the SEAD database structure was created using the note-taking program, [Obsidian.](https://obsidian.md/), chosen for its graphical representation of the connections between notes._

[[index|Back to the Start page]]
