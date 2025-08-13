Apps Script toolkit for Las Vegas/Henderson CRE prospecting. Pulls listings from a Google Sheet, geocodes, scores viability, exports GeoJSON for My Maps, builds a Slides pitch deck, and serves a heatmap UI inside the Sheet.

What this does
Geocode listings (Google Geocoding API) and cache results

Score & rank properties (size/lot/zoning/price/condition/parking → weighted total)

Export GeoJSON for My Maps (per-ZIP filter)

Auto-build Slides: title slide + “Top N” ranked table + optional static map image

Heatmap sidebar (Maps JS): visualize by ZIP, weighted by Total SF (with √ scaling)

Stack
Google Apps Script (V8) • Google Sheets • Google Slides • Google Drive • Google Maps (JavaScript, Geocoding, Static Maps)

A) Bound to a Sheet (fastest)
Open the target Google Sheet → Extensions → Apps Script.

Paste files from /src into the editor (keep filenames).

Put your Maps key in Project Settings → Script properties:

MAPS_API_KEY = <your key>

Back in the Sheet, reload. Use the Hiltz Tools menu:

Geocode → Score → Export GeoJSON → Build Slides

Open Heatmap to launch the sidebar
