---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity analysis_numerical_values.md
modified: 2026-09-17T15:51:56.806Z
---

> [!info] Percent of Modern Carbon
>
> - pMC\_value the measured amount of the percent of modern carbon
> - pMC\_error the error on that measurement
>
>   As these are analytically obtained values, and are in decimal format, I am assuming they will go to this table,
>   In the case of the pMC\_error, they will be assigned a ± [[qualifier]] through the creation of a new column using the code `=replace(replace(value_type_name,'pmc_value', ''), 'pmc_error', '±')`

> [!warning] I asked Phil about the difference between [[qualifier_id]], [[qualifier_symbol_id]], and [[cardinal_qualifier_id]] and when to use which
> The question was deferred to Roger. Still waiting for a decision on how we will do this as of 2026-09-17

# YAML as of 2026-09-17

````
name: analysis_numerical_value
type: entity
system_id: system_id
keys: []
columns:
  - unique_row_identifier
  - pmc_value
  - pmc_error
public_id: analysis_numerical_value_id
source: datasheet
foreign_keys:
  - entity: analysis_value
    local_keys:
      - unique_row_identifier
      - value_type_name
    remote_keys:
      - unique_row_identifier
      - value_type_name
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
      allow_unmatched_left: true
drop_empty_rows: true
unnest:
  id_vars:
    - unique_row_identifier
  value_vars:
    - pmc_value
    - pmc_error
  var_name: value_type_name
  value_name: value
extra_columns:
  qualifier: '=replace(replace(value_type_name,''pmc_value'', ''''), ''pmc_error'', ''±'')'
```
````
