---
Entity_Name: analysis_values
Type: Data (Derived)
Public_ID: "[[analysis_numerical_value_id]]"
Target_Entity:
Local_Keys:
  - 
  - 
  - 
Remote_Keys:
SEAD_table: "[[tbl_analysis_numerical_values]]"
status: in progress
publish: true
---
> [!info] Percent of Modern Carbon
> - pMC_value the measured amount of the percent of modern carbon
> - pMC_error the error on that measurement
>   
>   As these are analytically obtained values, and are in decimal format, I am assuming they will go to this table, 
>   In the case of the pMC_error, they will be assigned a `qualifer`based either on:
> - [[qualifier_symbol_id]]: 9   which is the symbol: ±  
> - [[qualifier_id]]: 11   which is the symbol: ±  (which is also [[cardinal_qualifier_id]]: 9 )


- [ ] create the data derived entity
- [ ] figure out how to have both the `pMC_value` and `pMC_error` entered into the table, each attached to the same sample
- [ ] add also the extra column `qualifer` to the rows with a `pMC_error` and fill it with the right code to get the ±



