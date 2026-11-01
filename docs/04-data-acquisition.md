# Data acquisition – what is still missing and where to get it

The cloud session that maintains this repo cannot reach `vpa.vic.gov.au`,
`casey.vic.gov.au`, `planning.vic.gov.au`, `data.vic.gov.au`, `opendata.maps.vic.gov.au`
or ArcGIS hosts (network policy and/or Cloudflare). It **can** reach the VPA's S3
document bucket (`vpa-web.s3.amazonaws.com`), which is where the plans added on
1–2 Nov 2026 came from.

Items below must be downloaded in a normal browser and pushed to `All Documents/`.

## 1. Current indexed rates – highest priority (calculator test data)

Casey publishes current rates for every plan. Save each page as PDF (Ctrl+P → Save
as PDF):

- DCP rates: <https://www.casey.vic.gov.au/development-contribution-plans-rates>
- ICP rates: <https://www.casey.vic.gov.au/infrastructure-contribution-plans-rates>

## 2. Missing plan documents

| Plan | Where |
|---|---|
| Minta Farm ICP – April 2021 (approved) | <https://vpa.vic.gov.au/project/minta-farm-icp/> |
| Croskell (Employment) ICP – October 2025 (approved) + PSP | <https://vpa.vic.gov.au/project/croskell/> |
| Cranbourne West DCP – current (VC249) version, if one exists | <https://vpa.vic.gov.au/project/cranbourne-west/> |
| Collison Estate DCP (DCPO22, C286case) | Casey Planning Scheme, Clause 72.04 incorporated documents |
| Fountain Gate–Narre Warren CBD DCP (DCPO20/21) | Casey Planning Scheme, Clause 72.04, or casey.vic.gov.au |
| Local Structure Plan 3 (Cranbourne East) DCP (DCPO4) | Casey Planning Scheme, Clause 72.04 |
| ICP and DCP Ministerial Directions | planning.vic.gov.au → Ministerial directions |

## 3. GIS data (all open, CC BY 4.0)

| Layer | Use | Where |
|---|---|---|
| Vicmap Planning – Planning Scheme Overlay Polygon | DCPO/ICO boundaries | <https://discover.data.vic.gov.au/dataset/vicmap-planning-planning-scheme-overlay-polygon> |
| VPA Precinct Boundaries | PSP/ICP precinct boundaries | <https://discover.data.vic.gov.au/dataset/vpa-precinct-boundaries> |
| Future Urban Structure Land Use | PSP land use (approved PSPs only) | <https://discover.data.vic.gov.au/dataset/fus-land-use> |
| Precinct Structure Plans – Road Centrelines | PSP road network (beta) | <https://discover.data.vic.gov.au/dataset/precinct-structure-plans-road-centrelines> |
| Vicmap Property – parcels | Current parcels | data.vic.gov.au (search "Vicmap Property parcel polygon") |

Vicmap statewide layers are large; clip to Casey before committing (the full
state overlay layer will exceed GitHub's 100 MB file limit). Preferred format:
GeoPackage or GeoJSON, GDA2020 (EPSG:7844 or 7855).

Field definitions for the VPA layers: `sources/gis/VPA-Precinct-Boundaries-Spatial-Data-Description-v5-2022.pdf`.

**Not publicly available (Casey confirmed it has no GIS for contributions):**
charge-area boundaries, PSP property-number ↔ current-parcel mapping, project
locations. These will have to be digitised from the DCP/PSP maps.
