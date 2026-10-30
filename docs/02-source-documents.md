# Source documents – theoretical backbone

Index page: <https://www.planning.vic.gov.au/guides-and-resources/legislation-regulation-and-fees/infrastructure-contributions>

**Access status (30 Oct 2026):** planning.vic.gov.au is behind a Cloudflare bot
challenge, so automated download is not possible. The PDFs need to be downloaded
manually and committed to `sources/` (see below).

## Register

| Doc | Framework | URL | In repo? |
|---|---|---|---|
| Infrastructure Contributions Plan Guidelines (Metropolitan Greenfield Growth Areas) | ICP | linked from the index page | ☐ |
| Ministerial Direction – Preparation, content and reporting requirements for ICPs (s46GJ, s46GZI) | ICP | [PDF](https://www.planning.vic.gov.au/__data/assets/pdf_file/0026/633545/Ministerial-Direction-Preparation-and-content-and-reporting-requirements-for-Infrastructure-Contributions-Plans.pdf) | ☐ |
| Whole-of-life land calculation example spreadsheets | ICP | linked from the index page | ☐ |
| Ministerial Direction – Preparation, content and reporting requirements for DCPs | DCP | [PDF](https://www.planning.vic.gov.au/__data/assets/pdf_file/0033/632598/Ministerial-Direction-Preparation-and-content-and-reporting-requirements-for-Development-Contributions-Plans.pdf) | ☐ |
| Development Contributions Guidelines – Understanding Development Contributions | DCP | [PDF](https://www.planning.vic.gov.au/__data/assets/pdf_file/0025/633373/Understanding-Development-Contributions-full.pdf) | ☐ |
| Development Contributions Guidelines – Preparing a Full Cost Apportionment DCP | DCP | [PDF](https://www.planning.vic.gov.au/__data/assets/pdf_file/0026/633374/Preparing_a_Full_Cost_Apportionment_DCP.pdf) | ☐ |
| Casey DCPs / ICPs (incorporated documents in the Casey Planning Scheme) | DCP/ICP | planning-schemes.app.planning.vic.gov.au | ☐ |

The list is not yet verified against the live index page; add anything missing.

## Why both DCP and ICP

*To verify against the Casey Planning Scheme:* Casey's growth areas are believed
to be covered by a mix of older DCPs and newer ICPs. The two
have different calculation logic (DCP: cost apportionment per charge area; ICP:
standard levy + supplementary levy + land equalisation). A Casey platform that only
models ICPs would miscalculate parcels in DCP areas.

## Suggested layout

```
sources/
  icp/   guidelines, ministerial direction, spreadsheets
  dcp/   guidelines, ministerial direction
  casey/ each Casey DCP/ICP incorporated document
```
