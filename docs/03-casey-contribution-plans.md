# Casey contribution plans – inventory

Source of the plan list: Casey Planning Scheme, last updated by **C302case on
22/07/2026** (`All Documents/Casey Planning Scheme-compressed.pdf`, 1,525 pp; text in
`sources/_text/Casey Planning Scheme-compressed.txt`). Schedule line numbers refer to
that text file.

Status key: ✅ current version in repo · 🟡 older / draft / interim version only ·
☐ not in repo. `SUPERSEDED-` / `DRAFT-` file-name prefixes mark non-current versions.

## Development Contributions Plan Overlay (Clause 45.06) – 13 DCPs

| DCPO | Plan | Amendment | Status | Location | Schedule line |
|---|---|---|---|---|---|
| 3 | Local Structure Plan 1 (Lyndhurst) DCP | C99 | ✅ Casey version, June 2026 | `All Documents/` | 40739 |
| 4 | Local Structure Plan 3 (Cranbourne East) DCP | — | ☐ | — | 40828 |
| 10 | Cranbourne East PSP DCP | C119 | ✅ May 2010, amended Dec 2023 (VC249) | `sources/casey/cranbourne-east/` | 40960 |
| 11 | Cranbourne North PSP DCP | C125 | ✅ June 2011, amended Dec 2023 (VC249) | `sources/casey/cranbourne-north/` | 41087 |
| 12 | Cranbourne West DCP | C206 | 🟡 Aug 2015, amended Aug 2017 (VC249 version not found) | `sources/casey/cranbourne-west/` | 41269 |
| 13 | Clyde North PSP DCP | C259case | ✅ Aug 2011, amended Dec 2023 (VC249) | `sources/casey/clyde-north/` | 41515 |
| 14 | Botanic Ridge DCP | C265case | ✅ Dec 2012, amended Dec 2023 (VC249) | `sources/casey/botanic-ridge/` | 41630 |
| 15 | Clyde DCP | C187 | ✅ Oct 2014, amended Dec 2023 (VC249), Parts 1–3 | `All Documents/` | 41736 |
| 18 | Berwick Waterways DCP | C188 | ✅ Oct 2014, amended Dec 2023 (VC249) | `sources/casey/berwick-waterways/` | 41885 |
| 19 | Brompton Lodge DCP | C190 | ✅ Aug 2016, amended Dec 2023 (VC249) | `sources/casey/brompton-lodge/` | 42023 |
| 20 | Fountain Gate–Narre Warren CBD DCP – Area 1 | — | ☐ | — | 42132 |
| 21 | Fountain Gate–Narre Warren CBD DCP – Area 2 | — | ☐ | — | 42241 |
| 22 | Collison Estate DCP | C286case | ☐ | — | 42351 |

## Infrastructure Contributions Overlay (Clause 45.11) – 3 ICPs

| ICO | Plan | Status | Location | Schedule line |
|---|---|---|---|---|
| 1 | Cardinia Creek South ICP (March 2019) | ✅ March 2019 (gazetted Apr 2019) + PSP amended March 2026 | `sources/casey/cardinia-creek-south/` | 42840 |
| 2 | Minta Farm ICP (April 2021) | 🟡 only the superseded interim May 2019 ICP | `sources/casey/minta-farm/` | 43014 |
| 3 | Croskell (Employment) ICP (October 2025) | 🟡 only the Sept 2024 consultation draft | `sources/casey/croskell/` | 43179 |

Clause 72.04 (incorporated documents) schedule starts at line 67389.

## Notes

- **13 DCPs vs 3 ICPs**, consistent with the 2024-25 annual report (DCP receipts
  $74.5m vs ICP $24.4m).
- **CIL wording is stale in the plan documents.** The DCPs still quote the old
  $1,150/dwelling CIL cap; the cap is indexed annually ($1,590 in 2026-27). The
  calculator must take current rates from Casey's published rate tables, not the
  plan text.
- **C208 Clyde Creek DCP (Oct 2015)** in `All Documents/` has the same cover as the
  current Clyde DCP and appears to be an earlier version. *To verify.*
- Rates in each DCP are in base-year dollars (e.g. Cranbourne North: $199,730 /
  $83,923 per NDHa by charge area). Indexed current rates are published by Casey —
  see `docs/04-data-acquisition.md`.

## Suggested build order

1. **Cranbourne East DCP (DCPO10)** – full DCP + PSP land budget in repo.
2. **Clyde DCP (DCPO15)** – full DCP in repo; larger and more recent.
3. **Cardinia Creek South ICP (ICO1)** – the one ICP with a current version in repo;
   pairs with the WOL example spreadsheets for land equalisation.
