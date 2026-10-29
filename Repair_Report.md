# NSW data repair and map update — 29 October 2026

- 4,749 original postcode/locality entries retained.
- 244 of the 475 held entries recovered for draft zoning; 4,518 entries now assigned.
- 231 entries remain held. Of these, 64 now have both CBD route scenarios and a contact reference. Alias/facility population is not replaced with a parent locality count.
- 11 postcode/ABS postal-area discrepancies resolved using exact locality names, postcode CSV identity and existing OSM named points inside the verified ABS locality boundary.
- 76 recovered route points use interior ABS locality proxies; 6 use checked postcode CSV coordinates. Proxy and approximate routes require address-level access validation and remain explicitly labelled in the workbook.
- Both CBD route modes were validated, with ferries excluded, no-toll segments checked, endpoint snapping capped at 2 km and road endpoints checked inside verified locality geometry where available. Nearest contacts use directed no-toll routes and geographic lower-bound screening. Routing is standard-car/free-flow, not truck routing or live traffic.
- All previous eligible distance-zone letters retained. Seven gap/extension bands (AC–AI) bring the continuity allocation to 35 zones, each <=40 km planning-distance spread. Added letters are not distance-ordered; read the numeric ranges. A complete regrouping could use 31 bands but would change existing letters.
- Modelled contact-catchment populations recomputed from unique ABS SAL codes. Total population reconciles to 8,069,912 (2021 Census reference). Griffith changed from M to C under the existing catchment threshold after population recovery; no thresholds were changed.

## Files

The revised workbook preserves the original worksheets and adds Data repair, with before/after status, routing-point source and remaining issues for all 475 original held entries.

Remaining_Locality_Review.csv lists the 231 remaining held entries. Blank numeric cells mean unavailable, not zero. Outside_Coverage_Boundaries.csv lists population-base localities without a matched coverage entry, including non-spatial statistical categories; these are not automatically delivery destinations.

## Source checks

NSW_Regional_Population_Master.xlsx was reread and its unique-locality populations reconcile to the existing population base. NSW_Postcodes_Radius_Zone_Mapping.xlsx was reread for postcode and representative-point context; radius distances are not substituted for road kilometres. australian-postcodes.csv supplies checked candidate coordinates / postcode identity. Boundaries are the bundled official ABS ASGS 2021 SAL geometry. Road data are the existing Geofabrik NSW OSM extract downloaded 28 October 2026, routed locally with Valhalla.

Original source workbooks in Downloads were not overwritten. The original analysis workbook remains preserved; the live repository source.xlsx is a copy of the revised workbook.

## Map additions

Compare multiple distance zones using the zone checkboxes and Show selected zones. Add multiple suburbs, postcodes or full named clusters in Compare multiple areas. Blue comparison outlines remain visible across filters; remove individual selections, zoom to all or clear them. The original single-result zoom, details and pulsing highlight remain available. Grey boundaries outside the coverage table show available population-base context on click, with unavailable route / postcode fields clearly identified.
