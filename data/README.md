# Data directory

This folder holds the input data files used by the notebook.

## Files included

- `soois.csv` — Suspected Non-Fatal Opioid Overdoses in Shelters (City of Toronto open data)
- `geocoded_addresses.csv` — Geocoded coordinates for unique shelter/supportive housing addresses (cached to avoid re-querying Nominatim)
- `toronto_neighbourhoods.geojson` — 158-neighborhood model boundaries (City of Toronto open data)

## File you need to download separately

The 2021 Census Neighbourhood Profiles file is large and ships in `.xlsx` format. To reproduce the spatial regression in Section 8.5:

1. Visit https://open.toronto.ca/dataset/neighbourhood-profiles/
2. Download the 2021 Census profile (158-neighborhood model)
3. Save it to this folder as `neighbourhood-profiles-2021-158-model.xlsx`

The notebook reads it via `pd.read_excel(...)` in Section 8.5.4.
