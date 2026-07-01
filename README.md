# pbi-templates

Power BI dashboard templates and standards for Scripps.

## Repository Structure

```
.github/
  copilot-instructions.md     # GitHub Copilot standards (auto-loaded in every session)
docs/
  naming-conventions.md       # File, tab, measure, and column naming rules
  style-guide.md              # Colors, fonts, layout standards
checklists/
  new-dashboard-checklist.md  # Pre-publish checklist for every dashboard
templates/
  standard-dashboard/         # Starter .pbit template files
  tab-layouts/                # Reference layouts for common tab types
```

## Quick Start

1. Copy the checklist from `checklists/new-dashboard-checklist.md`
2. Follow `docs/naming-conventions.md` for all file/measure/tab names
3. Follow `docs/style-guide.md` for colors, fonts, and layout
4. Add your dashboard `.pbix` file to a project folder (not this repo directly)
5. Open a Copilot session — `copilot-instructions.md` loads automatically

## Standards Summary

- **Primary color**: `#3257A8` (Scripps Blue)
- **Font**: Arial, 8pt, black/dark gray
- **Required tabs**: User Reference, Version Notes
- **Required elements per tab**: Dashboard name header, tab name header, data refresh date, support mailto link, Reset Filters button

See `docs/` for full details.
