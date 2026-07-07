# dbt_starter_project v0.1.3
## Schema/Data Change (--full-refresh required after upgrading)
**2 total changes • 1 possible breaking change** — tests bold, bullet character, H2 with parenthetical (awk must not mistake subheadings for version boundaries)

| Data Model(s) | Change type | Old | New | Notes |
| ------------- | ----------- | --- | --- | ----- |
| `my_model` | Column added | — | `new_col` | Tests pipe characters and backticks inside a table |
| `my_model` | Column renamed | `old_name` | `new_name` | **Tests bold inside a table cell** |

## Bug Fix
- Tests double quotes, backslash, and HTML entity: records with `status = "cancelled"` and path `C:\data\` were dropped when `&` was present in the filter.

## Feature Update
- Tests fenced code block with quotes inside — the following query was incorrectly rejected:
  ```sql
  select * from my_model where status = "active" and path = "C:\data\"
  ```

> Tests blockquote with bold: **Note** that `>` must not be treated as shell redirection inside the heredoc.

## Under the Hood
- Tests contributor link stripping vs PR link preservation: ([#1](https://github.com/fivetran-catfritz/release-tester-update/pull/1) [@catfritz](https://github.com/catfritz)) — sed should strip `[@catfritz](url)` but leave `[#1](url)` alone.

# dbt_starter_project v0.1.1
- test release 2

# dbt_starter_project v0.1.0
- test release