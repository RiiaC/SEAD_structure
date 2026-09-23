---
publish: true
permalink: /Example dataset mapping/Strucke Data-mapping/Entity site_property.md
modified: 2026-09-22T06:29:41.998Z
---

> \[!to do] The relevant columns for this dataset relating to site properties are:
>
> - **raa\_id** = [[site_property]], where [[property_type]] = RAÄ\_number
> - **site\_type** = [[site_property]], where [[property_type]] = type\_of\_site
> - **uppdragsnummer** = [[site_property]], where [[property_type]] = uppdragsnummer (the official government number on record for a specific Swedish archaeological excavation)
> - **lämningsnummer** = is a [[national_site_identifier]], but is likely to go into the new [[site_property]] table with [[property_type]] = to lämningsnummer. Note: this is also what we are using for [[site_name]], if one is listed.

> \[! note]   This entity requires a "unnest" function
> Some sites had multiple [[lämningsnummer]] and [[uppdragsnummer]] so they have been split in  [[Entity supersite]] into multiple columns each before coming to this table. now it is necessary to make multiple rows of them

## unnest

| ID Variables | _(columns to keep as is)_<br>Value Variables                                                                                                                                                        | _(columns to unpivot)_<br>Variable Name Column | _(name for the new column containing variable names)_<br>Value Name Column |
| ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------- | -------------------------------------------------------------------------- |
| [[site_key]] | [[lamningsnummer_1]]<br>[[lamningsnummer_2]]<br>[[lamningsnummer_3]]<br>[[lamningsnummer_4]]<br>[[uppdragsnummer_1]]<br>[[uppdragsnummer_2]]<br>[[uppdragsnummer_3]]<br>[[site_type]]<br>[[raa_id]] | [[property_type]]                              | [[property_value]]                                                         |

## formula for the [[property_type_id]] extra column

```
=to_int(replace(replace(replace(replace(replace(replace(replace(replace(replace(property_type, 'lamningsnummer_1', '4'), 'lamningsnummer_2', '4'), 'lamningsnummer_3', '4'), 'lamningsnummer_4', '4'), 'uppdragsnummer_1', '3'), 'uppdragsnummer_2', '3'), 'uppdragsnummer_3', '3'), 'site_type', '2'), 'raa_id', '1')) 
```

## replace

- [ ] Figure out where Bruno was going with this, it doesn't look complete
  (sent a message2026-09-22)

| columns                                                                                                                                                                                                                                     | replacments                      |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
| [[site_key]]<br>[[lamningsnummer_1]]<br>[[lamningsnummer_2]]<br>[[lamningsnummer_3]]<br>[[lamningsnummer_4]]<br>[[uppdragsnummer_1]]<br>[[uppdragsnummer_2]]<br>[[uppdragsnummer_3]]<br>[[site_type]]<br>[[raa_id]]<br>[[property_type_id]] | No rules configured for site\_key |
|                                                                                                                                                                                                                                             |                                  |
|                                                                                                                                                                                                                                             |                                  |

# YAML as of 2026-09-22

````
name: site_property
type: entity
system_id: system_id
keys: []
columns:
  - site_key
  - lamningsnummer_1
  - lamningsnummer_2
  - lamningsnummer_3
  - lamningsnummer_4
  - uppdragsnummer_1
  - uppdragsnummer_2
  - uppdragsnummer_3
  - site_type
  - raa_id
public_id: site_property_id
source: supersite
foreign_keys:
  - entity: property_type
    local_keys:
      - property_type_id
    remote_keys:
      - property_type_id
    how: inner
    constraints:
      cardinality: one_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
  - entity: site
    local_keys:
      - site_key
    remote_keys:
      - site_key
    how: inner
    constraints:
      cardinality: many_to_one
      allow_unmatched_right: true
      require_unique_left: false
      require_unique_right: false
      allow_row_decrease: true
drop_duplicates: true
check_functional_dependency: false
drop_empty_rows:
  - property_value
unnest:
  id_vars:
    - site_key
  value_vars:
    - lamningsnummer_1
    - lamningsnummer_2
    - lamningsnummer_3
    - lamningsnummer_4
    - uppdragsnummer_1
    - uppdragsnummer_2
    - uppdragsnummer_3
    - site_type
    - raa_id
  var_name: property_type
  value_name: property_value
extra_columns:
  property_type_id: '=to_int(replace(replace(replace(replace(replace(replace(replace(replace(replace(property_type, ''lamningsnummer_1'', ''4''), ''lamningsnummer_2'', ''4''), ''lamningsnummer_3'', ''4''), ''lamningsnummer_4'', ''4''), ''uppdragsnummer_1'', ''3''), ''uppdragsnummer_2'', ''3''), ''uppdragsnummer_3'', ''3''), ''site_type'', ''2''), ''raa_id'', ''1''))'
```


````
