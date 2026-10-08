---
publish: true
permalink: /Structure of SEAD/Tables/Columns/qualifier_symbol_id.md
created: 2026-07-24T09:34:40.218Z
modified: 2026-09-29T10:43:55.394Z
published: 2026-09-29T10:43:55.394Z
connected_tables:
  - "[[tbl_value_qualifier_symbols]]"
column_name: qualifier_symbol_id
data_type: integer
---

Primary key (automatically incremented).

> [!abstract] on 2026-09-29, when asked about the various levels of qualifier id's, Roger said:
> Yes, perhaps we should rename the columns, it felt logical when designed, but are a bit confusing. now. If I were to rename them, then it would be like this:
>
> - "qualifier" => "symbol"
> - "cardinal\_qualifier\_id" => "qualifier\_id"
>   The "tbl\_value\_qualifier\_symbols" is a lookup table containing all known symbols. Some of these symbols have the same meaning e.g. "!=" and "<>", "not equal". The purpose of the tbl\_value\_qualifiers lookup table is to group symbols by their meaning i.e. rows in tbl\_value\_qualifier\_symbols with the same "cardinal\_qualifier\_id" has the same semantic meaning.
