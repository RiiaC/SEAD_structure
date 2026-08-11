---
Entity_Name: methods
Type: Fixed Values
Public_ID: "[[method_id]]"
Target_Entity: "[[Entity method_groups]]"
Local_Keys:
  - "[[method_group_id]]"
Remote_Keys: "[[method_group_id]]"
publish: true
---
> [!info] there are several types of radiocarbon methods already in SEAD:|
> - **method_id:** method_name 
>  - **156:** Calibrated radiocarbon date (method unspecified)
>   - **157:** Calibrated AMS radiocarbon date 
>   - **149:** Radiometric date by unknown method 
>     
> **The first draft of data mapping will use 157**, until and unless I receive information suggesting I choose another

| New Column Name | Source Column |
| --------------- | ------------- |
| method_id       | 157           |

> [!warning]  figure out how to attach methods to the sample group!

![[Entity method_groups schema.png]]