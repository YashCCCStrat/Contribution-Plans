# Source documents – theoretical backbone

Index page: <https://www.planning.vic.gov.au/guides-and-resources/legislation-regulation-and-fees/infrastructure-contributions>
(planning.vic.gov.au blocks automated download, so documents are added manually.)

Originals live in `sources/<framework>/` and in `All Documents/` (the user's drop folder,
pushed directly); plain-text extracts for search in `sources/_text/`.

Also now in `All Documents/` (Nov 2026): full Casey Planning Scheme (C302case),
Clyde DCP Parts 1–3, Lyndhurst DCP (June 2026), C208 Clyde Creek DCP and PSPs
(Clyde Creek, Thompsons Road, Casey Fields South), Understanding Development
Contributions, both WOL land calculation spreadsheets, Benchmark Infrastructure
Costs Guide + 2026-27 indexation, Review of Benchmark Infrastructure Costings (2019),
GAIC model WIK agreement (land transfer). See `docs/03-casey-contribution-plans.md`.

## Register

| Doc | Framework | Version | In repo |
|---|---|---|---|
| DTP *Infrastructure contributions* page (print of index page) | All | Last updated 14 Oct 2026 | ✅ `sources/general/` |
| Infrastructure Contributions Plan Guidelines | ICP | March 2021 (DELWP), CC BY 4.0 | ✅ `sources/icp/` |
| Preparing a Full Cost Apportionment DCP | DCP | V5.9, March 2007 | ✅ `sources/dcp/` |
| GAIC Model Work-in-Kind Agreement (Land & Works) | GAIC | Draft, 2013–14 | ✅ `sources/gaic/` |
| Incorporating the DCP into the planning scheme | DCP | — | ✅ `sources/dcp/` |
| Planning Practice: Chapter 8 – Agreements (s173) | s173 | — | ✅ `sources/s173/` |
| Annual report on ICP and DCP levies 2024-25 (s46GZJ) | Reporting | FY 2024-25 | ✅ `sources/reporting/` |
| DTP *Growth areas infrastructure contributions* page | GAIC | Last updated 19 Jun 2026 | ✅ `sources/gaic/` |
| GAIC Work-in-Kind Guidelines | GAIC | — | ✅ `sources/gaic/` |
| GAIC WIK – Expression of Interest (works and land) | GAIC | — | ✅ `sources/gaic/` |
| GAIC WIK – Detailed proposal (land transfer) | GAIC | — | ✅ `sources/gaic/` |
| GAIC BNCF whole-of-program expenditure | GAIC | — | ✅ `sources/gaic/` |
| GAIC GAPTF whole-of-program expenditure | GAIC | — | ✅ `sources/gaic/` |
| Ministerial Direction – ICPs (s46GJ, s46GZI) | ICP | — | ☐ **critical** (sets standard levy rates, allowable items) |
| Ministerial Direction – DCPs | DCP | — | ☐ **critical** |
| IPPL only – example PSP – Whole of Life Land Calculation (XLSX) | ICP | — | ☐ **critical** (land equalisation worked example) |
| OPPL and IPPL – example PSP – Whole of Life Land Calculation (XLSX) | ICP | — | ☐ **critical** |
| Understanding Development Contributions | DCP | — | ☐ |
| Clyde DCP (Oct 2014, amended Dec 2023, VC249) — **Part 2 of 3** (from s7.6: interim road costings, per-metre cost estimates) | Casey DCP | Dec 2023 | ✅ `sources/casey/clyde/` — Parts 1 and 3 ☐ (Part 1 likely holds charge areas, levy rates, land budget) |
| Cranbourne East PSP (incl. Native Vegetation Precinct Plan) | Casey PSP | May 2010 | ✅ `sources/casey/cranbourne-east/` — has Plan 7 land budget and Table 4 property-specific land budget (NDA 467.66 ha) |
| **Cranbourne East DCP** (May 2010, amended Dec 2023, VC249) — complete, 39 pp | Casey DCP | Dec 2023 | ✅ `sources/casey/cranbourne-east/` — **first complete Casey test plan**. Demand unit = NDHa. Levies (base Jan 2010 $, before indexation): residential DIL $166,426/NDHa; employment DIL $101,575/NDHa; non-government education DIL $41,607/NDHa (25% of residential); CIL $735/dwelling. VC249 adds small-second-dwelling exemption. |
| Casey Planning Scheme (full, C302case 22/07/2026) | Casey | Jul 2026 | ✅ `All Documents/` |
| Casey GAIC project data (spatial.planning.vic.gov.au/gaic) | GAIC | — | ☐ (screenshot only) |

## Key facts from the index page (as of 14 Oct 2026)

**Casey is in scope for every contribution type:** DCP, ICP (Metropolitan Greenfield
Growth Areas — Casey is one of the seven growth councils), GAIC, public open space
(Subdivision Act s18) and s173 voluntary agreements. A Casey platform therefore
needs more than the DCP-only model in the Bass Coast reference portal.

| Mechanism | Overlay / basis | Levy basis |
|---|---|---|
| DCP | Clause 45.06 DCPO | Development infrastructure levy (uncapped, cost-apportioned) + community infrastructure levy (capped, per dwelling) |
| ICP | Clause 45.11 ICO | Standard levy (fixed by Minister, $/NDHa) + supplementary levy (bespoke) + land component (IPPL, land credit, land equalisation, OPPL) |
| GAIC | State levy | Collected by SRO (money) or VPA (land/works); funds Building New Communities Fund and Growth Areas Public Transport Fund |

### Reference rates (test data)

DCP community infrastructure levy cap ($/dwelling):
2021-22 $1,225 · 2022-23 $1,253 · 2023-24 $1,346 · 2024-25 $1,450 · 2025-26 $1,530 · 2026-27 $1,590
(indexed 1 July by ABS PPI Non-Residential Building Construction, Victoria)

ICP standard levy – residential ($/NDHa):

| | 2023-24 | 2024-25 | 2025-26 | 2026-27 |
|---|---|---|---|---|
| Community & recreation construction | 101,299 | 109,088 | 115,453 | 119,682 |
| Transport construction | 141,107 | 147,562 | 150,295 | 155,579 |
| **Total** | 242,406 | 256,650 | 265,748 | 275,261 |

ICP standard levy – commercial & industrial ($/NDHa): transport only —
2022-23 129,862 · 2023-24 141,107 · 2024-25 147,562 · 2025-26 150,295 · 2026-27 155,579

Public land indexation factors (Casey/Cardinia): 2022 1.240 · 2023 1.020 ·
2024 1.070 · 2025 1.000 · 2026 1.030

GAIC rates ($/ha; PE Act s201RC):

| Land type | 2023-24 | 2024-25 | 2025-26 | 2026-27 |
|---|---|---|---|---|
| A (s201RC(2)) | 110,590 | 115,530 | 118,830 | 122,260 |
| B-1, B-2, C (s201RC(3)–(5)) | 131,360 | 137,230 | 141,150 | 145,220 |

### Casey contributions received, FY 2024-25 (annual report, s46GZJ)

| Stream | Cash | Land / works accepted | Land equalisation | Total | IPPL |
|---|---|---|---|---|---|
| ICP | $15,220,590 | $1,635,247 (WIK) | $7,528,357 | **$24,384,194** | 13.31 ha |
| DCP | $46,973,109 | $27,479,214 | — | **$74,452,324** | — |

Casey's DCP receipts were ~3× its ICP receipts in 2024-25 — legacy DCPs still
carry most of the money.

### Observation
The Bass Coast reference portal applies a CIL of **$1,460/dwelling for FY26/27**,
below the $1,590 cap. A DCP may set CIL below the cap, so this is not necessarily an
error — but it shows the platform must store each plan's own rate and indexation
method, not assume the cap.

## Document structure (for building the knowledge base)

**ICP Guidelines (2021)** — Part A *The ICP system* (principles, legal framework,
monetary component: standard / supplementary levy, indexation, works-in-kind,
allowable items; land component: public purpose land, land contributions model,
land credit & equalisation amounts, IPPL/OPPL valuation; collecting & development
agencies) · Part B *Implementing an ICP* (4 preparation steps, ICO, imposing and
collecting contributions, paying land credits, administration, reporting, financial
management) · Part C *Specified development settings* (Metropolitan Greenfield
Growth Areas: standard and supplementary rates, developer-provided works,
indexation, adjustment of land amounts) · Appendices A–B.

**Preparing a FCA DCP (2007)** — key concepts (DCP area, timeframe, analysis areas,
quantifying development, demand units, equivalence ratios, main catchment area,
external/future usage, levy per demand unit, charge areas) · 5 phases / 16 stages
of preparation.

**GAIC Model WIK Agreement** — template legal agreement for delivering land and
works in lieu of GAIC payment.
