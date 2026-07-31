# Immunopeptidome Atlas

An interactive, single-file dashboard for exploring an integrated HLA-C / MHC-I ligand dataset, built from 7 independent immunopeptidomics studies.

No install, no server, no dependencies to set up — just open the HTML file in a browser.

## What's inside

- **124,152 unique peptides** integrated from 7 source studies (BJORN, BRAUN ex vivo, BRAUN DT9, MOBBS, PRINZ, MANJA, STEVANOVIC)
- Measured and predicted HLA-C / MHC-I binding evidence
- Peptide length distributions (overall and per-source)
- HLA-C allele frequency chart
- Cross-source overlap matrix
- Sequence motif logos (9-mers), built from information content, chemistry-colored
- A searchable/filterable peptide explorer with Excel export

## How to use it

1. Open 'Disease-associated-Omnibus-of-MHC-I-Epitopes-DOME' in any modern browser (Chrome, Firefox, Edge, Safari)
2. That's it — everything runs client-side, all data is embedded in the file

## Exploring the data

Most charts and tables are clickable:

| Where | What clicking does |
|---|---|
| Cross-source overlap table | Filters the explorer to peptides shared by that pair of studies |
| HLA-C allele frequency bars | Filters the explorer to peptides carrying that allele |
| Binding evidence chart | Filters the explorer to peptides with that binder call |
| Peptide length chart | Filters the explorer to peptides of that length, and downloads them as `.xlsx` |
| Motif logo cards | Filters + downloads that source's 9-mers as `.xlsx` |

Use the **⬇ Download results (.xlsx)** button in the Peptide Explorer to export whatever is currently filtered/searched, at any time.

## Data files

| File | Description |
|---|---|
| `immunopeptidome_master_long.csv` | Long-format table — one row per (peptide, source, allele) observation |
| `immunopeptidome_peptide_rollup.csv` | One row per unique peptide, with sources/alleles/binder calls summarized |
| `immunopeptidome_atlas.html` / `DOME.html` | The interactive dashboard, with the rollup data embedded |

## Notes

- The dashboard is a single self-contained HTML file — all data and charts are embedded, so it works offline once downloaded.
- Charts use [Chart.js](https://www.chartjs.org/) and Excel export uses [SheetJS](https://sheetjs.com/), both loaded from a CDN.
