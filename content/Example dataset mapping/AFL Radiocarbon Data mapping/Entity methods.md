---
publish: true
permalink: /Example dataset mapping/AFL Radiocarbon Data mapping/Entity methods.md
---

> [!info] there are several types of radiocarbon methods already in SEAD:|
>
> - **method\_id:** method\_name
> - **156:** Calibrated radiocarbon date (method unspecified)
> - **157:** Calibrated AMS radiocarbon date
> - **149:** Radiometric date by unknown method
>
> **The first draft of data mapping will use 157**, until and unless I receive information suggesting I choose another

| New Column Name | Source Column |
| --------------- | ------------- |
| method\_id       | 157           |

> [!warning]  figure out how to attach methods to the sample group!

![[images/Entity method_groups schema.png]]
