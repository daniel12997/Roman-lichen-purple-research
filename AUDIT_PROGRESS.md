# Audit Progress — Roman Lichen Purple Research

Auditing `roman_lichen_purple_dye_resources.md` against the primary-source corpus at `research_documents/*.pdf`.

## Input inventory

- **Survey file:** `roman_lichen_purple_dye_resources.md` (413 lines, already markdown — no Stage 0 conversion needed)
- **Per-paper summaries:** `.work/stage4/*.md` (85 files — prior Stage 4 from the bibliography pipeline)
- **Primary-source PDFs (13):**
  1. `Aceto_2015_SAA_folium_orchil_diagnostic.pdf` — orchil / folium analytical
  2. `Bicchieri_2014_ESPR_Codex_Rossanensis.pdf` — Rossano purple codex
  3. `Ferreira_2004_ChemSocRev_natural_constituents_historical_dyes.pdf` — **MISLABELED**: local file is Hulme et al. flavonoid conference paper; audit intended CSR review content via abstract only
  4. `Frezza_2024_Pharmaceutics_Roccella_tinctoria.pdf` — *R. tinctoria* phytochemistry
  5. `Hofmann_Aceto_2020_Vienna_Genesis_OAPEN.pdf` — Vienna Genesis book
  6. `Lackner_2024_Heritage_lichen_tapestry.pdf` — Cloisters Heroes tapestry, lichen xanthones
  7. `Pliny_NH_Loeb_L353_books_8-11.pdf` — Pliny book 9 (murex)
  8. `Pliny_NH_Loeb_L394_books_33-35.pdf` — Pliny book 35 (pigments)
  9. `Reinhold_1969_ClassicalJournal_status_symbols.pdf` — Reinhold precursor article
  10. `Smith_1921_Lichens_Cambridge_Botanical_Handbooks.pdf` — classic botany with dye chapter
  11. `VerheckenLammens_2010_ATN51_Roman_tunics_purple.pdf` — late Roman Egyptian textiles
  12. `Whitworth_2025_Heritage_milking_orchil.pdf` — goat-milk orchil recipe reconstruction
  13. `Whitworth_Koren_2016_Ambix_Bedfords_Leeds.pdf` — Leeds Bedford orchil industry history
- **Paywalled-but-cited (audited from abstracts only):** see `research_documents/INDEX.md` Not-Downloaded table — 23 entries (Musso, Beecken, Wainwright, Clementi, Doherty, Witkowski, Serafini, Calà, Roca, Kok, Aceto 2019 Mythic, Walton/Taylor, Moulherat, Tehler series, Ertz, Grierson pair, Brough, Graves)

## Prior corrections from pipeline (should persist — do not re-introduce)

- Calà 2019 DOI: `10.1016/j.microc.2019.104140` (not `104081`)
- Aceto 2019 Mythic Dyes DOI: `10.1016/j.saa.2019.01.091` (not `10.1016/j.saa.2018.11.027`)
- Zaffino 2016 entry: REMOVED (unverifiable citation)

## Pipeline status

| # | Stage | Status | Artifact | Commit |
|---|-------|--------|----------|--------|
| 0 | Baseline (markdown already) | ✅ n/a | `roman_lichen_purple_dye_resources.md` | `2775965` (initial commit) |
| 1 | Per-paper fact-check (13 sonnet agents) | 🔄 in progress | `.work/stage9-audit/stage1-per-paper/*.md` | — |
| — | Correction Pass 1 | ⏳ pending | — | — |
| 2 | Topical group audit (4 opus agents) | ⏳ pending | `.work/stage9-audit/stage2-groups/*.md` | — |
| — | Correction Pass 2 | ⏳ pending | — | — |
| 3 | Citation tracking (1 agent) | ⏳ pending | `.work/stage9-audit/stage3-citations/report.md` | — |
| 4 | Citation verification (3 opus agents) | ⏳ pending | `.work/stage9-audit/stage4-verification/*.md` | — |
| — | Correction Pass 3 | ⏳ pending | — | — |

## Error tallies (filled as stages complete)

_per-stage counts of misattributions, fabrications, omissions, drift to be filled_
