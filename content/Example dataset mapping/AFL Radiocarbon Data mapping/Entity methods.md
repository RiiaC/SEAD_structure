---
publish: true
permalink: /Example dataset mapping/AFL Radiocarbon Data mapping/Entity methods.md
created: 2026-07-24T09:34:07.983Z
modified: 2026-09-23T05:19:00.098Z
published: 2026-09-23T05:19:00.098Z
Entity_Name: methods
Type: Fixed Values
Public_ID: "[[method_id]]"
Target_Entity: "[[Entity method_groups]]"
Local_Keys:
  - "[[method_group_id]]"
Remote_Keys: "[[method_group_id]]"
change_it: true
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
