---
Entity_Name: features
Type: Data (Derived)
Public_ID: "[[feature_id]]"
Target_Entity: "[[content/Example dataset mapping/Strucke Data mapping/first draft of dataset/Entity feature_types]]"
Local_Keys:
  - system_id
Remote_Keys: "[[feature_type_id]]"
SEAD_table: "[[tbl_features]]"
status: ask if you did this right
---
> [!info] the list of archaeological features associated with the samples is recorded in three columns:
> - Anlnr (e.g. A9, A256, R2) = [[feature_name]], which goes in this Entity
> - anlaggning (e.g. Stolphål, Brunn) = [[feature_type_name]], which is part of [[content/Example dataset mapping/Strucke Data mapping/first draft of dataset/Entity feature_types]]
> - fornlamningstyp (e.g. boplats, hög, härd)

- [x] create a data-derived entity features, with feature_id
- [x] join it with the feature_type list based on the column anlaggning

>

![[Entity features schema.png]]

