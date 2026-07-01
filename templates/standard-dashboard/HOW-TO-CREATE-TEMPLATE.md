# How to Create the Standard Dashboard .pbit Template

A `.pbit` file must be exported from Power BI Desktop. Follow these steps to prepare
your existing `.pbix` and export a clean, reusable template.

---

## Step 1 — Prep Your .pbix for Export

Before exporting, clean the file so the template is data-agnostic and safe to share.

### Remove live data connections
- Go to `Home > Transform Data > Data Source Settings`
- Note all data sources — the template will prompt users to reconnect on first open
- If using Snowflake or other enterprise sources, this is fine to leave (users will authenticate)
- **Remove or blank out any manually entered/hardcoded sample data**

### Reset all slicers and filters to default state
- Clear all slicer selections so the template opens in a neutral state
- This becomes the default state your bookmarks capture

### Reset bookmarks
- `View > Show Panes > Bookmarks`
- Update each page's "Default" bookmark to reflect the clean, reset state
- This ensures RESET FILTERS works correctly from first use

### Check the header fields
- Replace real dashboard name with a placeholder: `[Dashboard Name]`
- Replace real tab names with placeholders: `[Tab Name]`
- Replace real dates with placeholders or remove them
- Replace real email/WKBK code in mailto link: `mailto:analyst@scripps.com?subject=Question regarding WKBK-000000`

### Review for sensitive data
- Remove any actual employee names, financials, or PII from sample rows
- If the model has imported data (not DirectQuery), clear the data cache:
  `File > Options and Settings > Options > Current File > Data Load > uncheck "Allow data preview to be downloaded..."`
  Or simply delete imported tables and leave the query structure intact

---

## Step 2 — Verify Required Elements Are Present

Before exporting, confirm your file has all required template elements:

- [ ] Scripps lighthouse logo (top left, all tabs)
- [ ] Primary header placeholder (Dashboard Name)
- [ ] Secondary header placeholder (Tab Name)
- [ ] Data Through date placeholder
- [ ] Last Refreshed date placeholder
- [ ] Support email `mailto:` link with placeholder WKBK code
- [ ] RESET FILTERS button (with bookmark assigned)
- [ ] `User Reference` tab (pre-formatted, placeholder text)
- [ ] `Version Notes` tab (pre-formatted with version table)
- [ ] Scripps blue (`#3257A8`) theme applied
- [ ] Arial font, 8pt, dark text throughout
- [ ] 5pt internal padding on all boxes
- [ ] 1pt dark gray border on all boxes

---

## Step 3 — Export as .pbit

1. In Power BI Desktop, go to `File > Export > Power BI Template (.pbit)`
2. In the description field, enter:
   ```
   Scripps standard dashboard template. Includes required headers, support link,
   Reset Filters button, User Reference tab, and Version Notes tab.
   Built to Scripps branding standards (blue #3257A8, Arial 8pt).
   ```
3. Save as: `TEMPLATE_Standard-Dashboard.pbit`

---

## Step 4 — Add to This Repository

1. Place the exported file here:
   ```
   templates/standard-dashboard/TEMPLATE_Standard-Dashboard.pbit
   ```
2. Fill in the metadata file at:
   ```
   templates/standard-dashboard/template-metadata.md
   ```
3. Commit and push:
   ```bash
   git add templates/standard-dashboard/
   git commit -m "Add standard dashboard .pbit template"
   git push
   ```

---

## Step 5 — Using the Template for New Dashboards

When starting a new dashboard:
1. Open `TEMPLATE_Standard-Dashboard.pbit` in Power BI Desktop
2. Connect to your data source when prompted
3. Replace all placeholder text (Dashboard Name, Tab Name, WKBK code, email)
4. Add your visuals and data tabs
5. Update bookmarks for each new tab's RESET FILTERS button
6. Save as a new `.pbix` with the naming convention: `WKBK-XXXXXX_Descriptive-Name.pbix`
