# Power BI Naming Conventions — Scripps

## Files
| Type | Convention | Example |
|------|-----------|---------|
| Dashboard file | `WKBK-XXXXXX_Descriptive-Name.pbix` | `WKBK-001234_Sales-Performance.pbix` |
| Template file | `TEMPLATE_Descriptive-Name.pbit` | `TEMPLATE_Standard-Dashboard.pbit` |
| Published report | Match `.pbix` filename | `WKBK-001234_Sales-Performance` |

## Tabs / Pages
- Use Title Case
- Be descriptive and user-friendly
- Required tabs: `User Reference`, `Version Notes`
- Data tabs: named after the view/cut (e.g., `Monthly Trend`, `Regional Breakdown`)

## Measures (DAX)
| Convention | Example |
|-----------|---------|
| `[Measure Name]` in Title Case | `[Total Revenue]`, `[YTD Sales]` |
| Prefix variance measures with `Var` | `[Var vs Budget]` |
| Prefix % measures with `%` or `Pct` | `[% Margin]`, `[Pct Attainment]` |
| Prefix conditional formatting measures with `CF_` | `[CF_Variance Color]` |

## Columns (in data model)
- Title Case, spaces allowed
- No underscores in display names
- Example: `Sales Region`, `Transaction Date`, `Product Category`

## Tables (in data model)
- Title Case, singular nouns
- Fact tables: prefix with `Fact_` → `Fact_Sales`
- Dimension tables: prefix with `Dim_` → `Dim_Customer`, `Dim_Date`
- Bridge/helper tables: prefix with `Bridge_` or `Calc_`

## Bookmarks
- Name by tab + state: `[Tab Name] - Default`
- Example: `Monthly Trend - Default`, `Regional - Filtered by West`

## Buttons
- Use plain action labels: `RESET FILTERS`, `GO TO OVERVIEW`, `DOWNLOAD`
