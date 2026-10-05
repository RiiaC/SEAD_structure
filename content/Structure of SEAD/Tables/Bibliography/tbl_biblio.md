---
publish: true
permalink: /Structure of SEAD/Tables/Bibliography/tbl_biblio.md
created: 2026-07-24T09:34:40.927Z
modified: 2026-10-02T09:16:36.816Z
published: 2026-10-02T09:16:36.816Z
table_name: tbl_biblio
primary_key: "[[biblio_id]]"
columns:
  - "[[biblio_uuid]]"
  - "[[bugs_reference]]"
  - "[[date_updated]]"
  - "[[doi]]"
  - "[[full_reference]]"
  - "[[isbn]]"
  - "[[notes]]"
  - "[[title]]"
  - "[[url]]"
  - "[[year]]"
  - "[[node_modules/buffer/AUTHORS|authors]]"
---

> [!info] Central repository for storing bibliographic references in the SEAD database. It stores detailed citations, including author, title, year, publisher, and DOI/URL for various sources such as books and articles. This table connects to domain-specific tables via foreign keys, ensuring data integrity and supporting research by centralizing bibliographic information.
