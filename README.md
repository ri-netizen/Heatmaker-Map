Apps Script toolkit for Las Vegas/Henderson CRE prospecting. Pulls listings from a Google Sheet, geocodes, scores viability, exports GeoJSON for My Maps, builds a Slides pitch deck, and serves a heatmap UI inside the Sheet.

What this does:
Geocode listings (Google Geocoding API) and cache results.

Score & rank properties (size/lot/zoning/price/condition/parking → weighted total).

Export GeoJSON for My Maps (per-ZIP filter).

Auto-build Slides: title slide + “Top N” ranked table + optional static map image.

Heatmap sidebar (Maps JS): visualize by ZIP, weighted by Total SF (with √ scaling).

Stack:

Google Apps Script (V8) • Google Sheets • Google Slides • Google Drive • Google Maps (JavaScript, Geocoding, Static Maps)

Set up A) Bound to a Sheet
1. Open the target Google Sheet → Extensions → Apps Script.

2. Paste files from /src into the editor (keep filenames).

3. Put your Maps key in Project Settings → Script properties: MAPS_API_KEY = <your key>
4. Back in the Sheet, reload. Use the Hiltz Tools menu:
   Geocode → Score → Export GeoJSON → Build Slides
   Open the Heatmap to launch the sidebar

Troubleshooting
“This page can’t load Google Maps correctly” → bad referrer or billing off. Fix API key restrictions as above.

Heatmap shows “Points: 0” → no rows match your ZIP filter or Lat/Lng empty. Run Geocode or clear ZIPs to show all.

Slides errors about resizing text/table → this project avoids clear() and table resizing; keep PredefinedLayout.BLANK and only set left/top.
