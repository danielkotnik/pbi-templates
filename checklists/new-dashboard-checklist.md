# New Dashboard Checklist — Scripps Power BI

Use this checklist before publishing any dashboard to production.

---

## Setup
- [ ] WKBK Asset Code assigned by Data Steward and noted in filename
- [ ] `.pbix` file named following convention: `WKBK-XXXXXX_Descriptive-Name.pbix`
- [ ] Scripps lighthouse logo placed at top left
- [ ] Scripps blue (`#3257A8`) used as primary color in visuals
- [ ] Theme applied (`View > Themes`) that minimizes visual distraction
- [ ] White or very light gray background used (no busy background images)

## Typography & Layout
- [ ] Font is Arial (or Helvetica/Roboto as fallback — Mac-safe)
- [ ] Default font size is 8pt
- [ ] Text color is black or dark gray
- [ ] All boxes have consistent exterior padding (Snap to Grid enabled)
- [ ] All boxes have 5pt internal padding
- [ ] All boxes have dark gray, 1pt outline

## Every Tab (Data Tabs)
- [ ] Primary header: Dashboard name
- [ ] Secondary header: Tab/worksheet name
- [ ] Max data date shown (if applicable)
- [ ] Semantic model last refresh date shown (if applicable)
- [ ] Support email displayed as `mailto:` link with correct WKBK subject line
- [ ] RESET FILTERS button present (if tab has slicers/filters)
- [ ] Bookmark set for RESET FILTERS button default state
- [ ] All slicer/filter labels are descriptive and user-friendly
- [ ] All visual titles are descriptive and user-friendly
- [ ] Red used only for warnings or unfavorable variance

## Required Tabs
- [ ] **User Reference tab** includes:
  - [ ] Data Asset ID
  - [ ] Business owner(s)
  - [ ] Data sources listed
  - [ ] Data lineage/dependencies described
  - [ ] Refresh schedule documented
  - [ ] FAQs / user guidance included
- [ ] **Version Notes tab** includes:
  - [ ] Initial version entry with date and author
  - [ ] Description of what the dashboard covers

## Data Model
- [ ] Tables named with `Fact_` / `Dim_` prefixes
- [ ] Measures named in Title Case per naming conventions
- [ ] Conditional formatting measures prefixed with `CF_`
- [ ] No sensitive or PII data exposed without approval

## Publishing
- [ ] Dashboard tested on a Mac (font rendering check)
- [ ] Shared with correct workspace/audience
- [ ] Data refresh schedule configured in Power BI Service
- [ ] Entry created or updated in Scripps Data Catalog
