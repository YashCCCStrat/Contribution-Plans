# Reference portal breakdown (Parsel DCP portal)

Reference: `https://portal.parsel.online/ad5e6b57-8a76-48c4-aa73-f83bb860ecfa`
Observed: 30 Oct 2026, headless Chromium, public (no login).

> **Scope of this note.** This records the portal's *functional* structure so we can
> design an equivalent for City of Casey. It is not a spec to copy Parsel's UI,
> branding or code — the platform is a commercial product of Mesh Dash Pty Ltd.
>
> **Evidence status.** The app shell, layout and tool panels were observed directly.
> The map layers and data were **not** observed: the portal's backend (a Supabase
> database + GeoServer) and Mapbox were blocked by the session's network policy, so
> every data panel rendered empty. Items marked *(inferred)* come from the names of
> the API requests the app attempted, not from returned data.

## 1. Technology (observed)

| Layer | What the portal uses |
|---|---|
| Front end | Angular single-page app, Tailwind CSS, light/dark theme |
| Map | Mapbox GL JS v2.6.1 (OpenStreetMap base) |
| Data API | Supabase (PostgREST over PostgreSQL) — tables/views queried by `plan_id` |
| Spatial layers | GeoServer, accessed via a per-plan key (`rpc/geoserver_plan_key`) |

One URL = one contribution plan (the UUID in the path is the `plan_id`).

## 2. Screen layout (observed)

```
┌────┬──────────────────────────────────────────────┬──────────────────────┐
│Tool│                                              │ Hover Info           │
│bar │              Full-screen map                 │  Property            │
│    │   (parcels, charge areas, projects)          │  NDA (ha)            │
│ 1  │                                              │  Charge Area(s)      │
│ 2  │                                              │  Project             │
│ 3  │                                              │  Total Cost          │
│ 4  │                                              ├──────────────────────┤
│    │                                              │ Key – Land Use   ▾   │
│ ✕  │                                              │ Key – Infrastructure▾│
└────┴──────────────────────────────────────────────┴──────────────────────┘
 Footer: Help · About · Disclaimer · Contact
```

On first load a modal **Acknowledgement of Use** (as-is, no warranty, rely at own
risk) must be accepted with **OK**.

### Hover Info panel
Updates as the cursor moves over the map:
- **Property** – parcel identifier
- **NDA (ha)** – Net Developable Area of the parcel
- **Charge Area(s)** – which DCP/ICP charge area(s) the parcel falls in
- **Project** – infrastructure project under the cursor
- **Total Cost** – that project's cost

### Legends
- **Key – Land Use** – land-budget categories (styled per plan: `plan_land_use_style`)
- **Key – Infrastructure** – project types (styled per plan: `plan_project_style`)

## 3. Left toolbar – four tools (observed)

| # | Tool | Content |
|---|---|---|
| 1 | **Summary** | Lists selected **Properties** and selected **Projects**, each with *Clear All*. |
| 2 | **Land Budget** | *Select Property ID/s* → **Property Land Budget Summary**: Total Area, Total Net Developable Area, Unencumbered Land, Encumbered Land (ha) … |
| 3 | **Estimate** (contribution calculator) | *Select Financial Year to continue* → **Property Details** (selected properties, Total NDA / demand units) → **Estimate Summary**: Total Liability, Total Credit, **Balance**; *Export*. |
| 4 | **Save and Share** | *Export to PDF* report of the selection; *Generate link* (shareable URL of the configuration); *QR code*. |

## 4. Data model (inferred from API calls)

| Endpoint | Probable meaning |
|---|---|
| `development_contribution_plan` | Plan register: name, gazettal date (`gazetted_at`), status |
| `plan_active_financial_years` | Financial years for which indexed rates exist |
| `dc_index_rate_levy` | Indexed levy rates per charge area / FY |
| `calculation_area_summary` (`current_au_fy=true`) | Per charge-area totals for the current Australian FY |
| `parcel_budget_final` | Property-specific land budget (gross, NDA, encumbered/unencumbered) |
| `dcp_property_details` | Parcel attributes (ID, charge area membership) |
| `plan_land_use_style`, `plan_project_style` | Map styling per plan |
| `dcp_map_initialization` | Initial map extent/zoom per plan (and a global default) |
| `rpc/dcp_init`, `rpc/geoserver_plan_key` | Bootstrap + access key for spatial layers |

### Implied calculation (inferred — verify against the plan documents)

```
liability  = Σ over charge areas ( parcel NDA in area × indexed levy rate for FY )
credit     = value of works-in-kind / land provided by the developer (from land budget)
balance    = liability − credit
```

## 5. What this means for a Casey platform

Core capabilities to reproduce (in our own design):
1. Per-plan map of parcels, charge areas and infrastructure projects
2. Parcel hover/click → land budget and charge-area membership
3. Multi-parcel selection → contribution estimate for a chosen financial year
4. Indexation of rates by financial year
5. Export (PDF/CSV) and shareable state (URL)
6. Disclaimer gating

Open gaps — need data access before they can be documented:
- Actual map layers and how projects are symbolised
- Exact fields in land budget and estimate outputs
- How credits (land vs works-in-kind) are calculated
- Whether the portal supports ICP (standard levy + land equalisation) or DCP only
