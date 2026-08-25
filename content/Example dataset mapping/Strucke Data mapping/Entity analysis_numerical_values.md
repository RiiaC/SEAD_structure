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
status: to troubleshoot
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

> [!note] Note: I asked Phil about the difference between [[qualifier_id]], [[qualifier_symbol_id]], and [[cardinal_qualifier_id]] and when to use which, and he deferred the question to Roger.


- [x] create the data derived entity
- [ ] figure out how to have both the `pMC_value` and `pMC_error` entered into the table, each attached to the same sample, and how to also record the fact that one is the value and the other is the error on the value
- [ ] figure out how to also add the extra column `qualifer` to the rows with a `pMC_error` and fill it with the right code (see above) to get the ±


# YAML as of 2026-08-25
````
name: analysis_numerical_values
type: entity
system_id: system_id
keys: []
columns:
  - pmc_value
  - pmc_error
  - lab_id
  - fid
public_id: analysis_numerical_value_id
source: datasheet_v9
drop_empty_rows:
  - pmc_value
unnest:
  id_vars:
    - lab_no
  value_vars:
    - pmc_value
    - pmc_error
  var_name: value_name
  value_name: value

```