# NSW postcode coverage

Interactive NSW delivery zone map. Select zones A–AB and consolidation classes C/M/R; search locality, postcode or cluster.

## Update assignments
Replace `source.xlsx` in this repository with the edited workbook, keeping the sheet names and columns. Commit, wait for Pages deployment, then reload the map. `NSW Postcode Coverage` controls assignments; `Locality analysis` supplies ABS SAL keys and reference details; `Cluster register` supplies contact points. The app reads saved values and does not recalculate Excel formulas or routes. Preview Excel file changes only your browser view.

`index.html` includes the map geometry and libraries. GitHub Pages reads `source.xlsx` directly. Opening index.html locally uses the original embedded snapshot; use Preview Excel file to load edits locally.

Boundaries: ABS ASGS 2021 Suburbs and Localities, downloaded 29 October 2026, generalised for display. https://geo.abs.gov.au/arcgis/rest/services/ASGS2021/SAL/MapServer/0
NSW outline: https://geo.abs.gov.au/arcgis/rest/services/ASGS2021/STE/MapServer/0
ABS copyright: https://www.abs.gov.au/website-privacy-copyright-and-disclaimer/copyright
Road references: © OpenStreetMap contributors, https://www.openstreetmap.org/copyright
Population references: 2021 Census. Catchment population is modelled, not official town population or observed order demand. Routes are reference estimates, not live traffic. This draft shows no rates. Boundaries do not guarantee service at every address.

Leaflet 1.9.4 (BSD-2-Clause) and fflate 0.8.2 (MIT) are embedded; licences included.


## Data repair and multiple selection (29 October 2026)

See [Repair report](Repair_Report.md). The revised source contains 4,518 assigned entries and 231 held entries. The Data repair worksheet records the evidence. Original letters A–AB remain; added bands AC–AI fill gaps or extend coverage. Use numeric distance ranges rather than alphabetic order for the new bands.

Compare multiple areas lets you select multiple zones or keep several suburbs, full postcodes and whole named clusters highlighted. The original search and details remain available. Grey boundaries with no coverage row show population-base context when available.


## Reference context and automatic comparison

Zone checkboxes update immediately. Comparison search suggests whole postcodes, clusters and localities. The source workbook adds Reference context and Online evidence: 230 held entries have geographic reference context; eight have explicitly unverified access-point models. Approximate postcode and parent-locality points are not exact facility addresses. Existing service assignments remain unchanged.
