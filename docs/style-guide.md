# Style Guide — Scripps Power BI Dashboards

## Color Palette

| Role | Hex | Usage |
|------|-----|-------|
| Scripps Blue | `#3257A8` | Primary charts, key highlights, headers |
| White | `#FFFFFF` | Page backgrounds |
| Light Gray | `#F2F2F2` | Secondary backgrounds, alternate rows |
| Dark Gray | `#404040` | Box outlines, secondary text |
| Black | `#000000` | Primary text |
| Red | `#C00000` | **Warnings and unfavorable variance ONLY** |

## Typography

| Element | Font | Size | Color |
|---------|------|------|-------|
| Body text | Arial | 8pt | Black / Dark Gray |
| Visual titles | Arial | 9–10pt | Black |
| Primary dashboard header | Arial | 14–16pt | Scripps Blue or Black |
| Secondary tab header | Arial | 11–12pt | Dark Gray |
| Support email link | Arial | 8pt | Scripps Blue (hyperlink) |

**Fallback fonts** (Mac-safe): Helvetica, Roboto
> ⚠️ Avoid non-Mac-safe fonts — they may render as Times New Roman on Mac.

## Layout Rules

- **Snap to Grid**: Always enable (`View > Page Options > Snap to Grid`)
- **Exterior padding**: Consistent on all containers
- **Internal padding**: 5pt on all boxes
- **Box borders**: Dark gray (`#404040`), 1pt

## Logo Placement

- Scripps lighthouse logo: top-left corner of every page
- Keep consistent size and position across all tabs

## Standard Page Header Layout

```
[ LOGO ]  [ Dashboard Name (Primary) ]          [ Last Refreshed: DATE ]
          [ Tab Name (Secondary) ]              [ Data Through: DATE   ]
                                               [ Contact: email@scripps.com ]
```

## Visual Best Practices

- Use bar/column charts for comparisons
- Use line charts for trends over time
- Use tables/matrices for detailed data
- Avoid pie charts for more than 3-4 categories
- Always include axis titles and data labels where helpful
- Avoid 3D effects on any visual

## Conditional Formatting

- **Favorable variance**: Scripps Blue or Green (avoid overusing green)
- **Unfavorable variance**: Red (`#C00000`)
- **Neutral**: Gray

Name all CF measures with `CF_` prefix (e.g., `[CF_Variance Color]`).
