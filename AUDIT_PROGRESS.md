# Audit Progress — Roman Lichen Purple Research (clean run 2026-04-23)

Auditing `roman_lichen_purple_dye_resources.md` (502 lines) against the primary-source corpus at `research_documents/*.pdf` (46 PDFs). This is a fresh audit pipeline; prior audit artifacts under `.work/stage9-audit/` are historical and not reused.

**Survey scope (per the document's own preamble):** primer / pointer list, NOT a research artifact. Calibrate "omission" flagging accordingly — missing synthesis appropriate only to a research artifact is NOT an error.

**Error scope (per user directive 2026-04-23):** flag ALL of the following, not only major errors:
- Major factual errors (misattribution, wrong sample counts, fabricated findings, wrong species/date/place)
- Minor factual errors (wrong figure numbers, wrong page ranges, small numerical slips, mild misparaphrases)
- Exaggeration / overstatement (claims going beyond what the source supports — e.g., "the single most important" when the source is modest; "established" / "demonstrated" when the source is tentative or one study; "all/every" when the source covers a sample; "first" when prior work exists; adjectival inflation in general)

Each agent should mark each finding with a severity: `MAJOR`, `MINOR`, or `OVERSTATEMENT`.

## Input inventory

- **Survey file:** `roman_lichen_purple_dye_resources.md`
- **Corpus:** 46 PDFs in `research_documents/` (see INDEX.md). No PDF → markdown conversion needed (survey already markdown).
- **Scratch directory:** `.work/audit/` (this run). Subdirectories per stage.
- **Concurrency cap:** 5 agents at a time (per user directive).

## Pipeline status

| # | Stage | Status | Artifacts | Commit |
|---|-------|--------|-----------|--------|
| 0 | Setup + baseline (markdown already) | ✅ done | — | — |
| 1 | Per-paper fact-check (46 sonnet agents, 5/wave) | ✅ done | `.work/audit/stage1-per-paper/*.md` (46 files + consolidated findings) | — |
| — | Correction Pass 1 (orchestrator edits) | 🔄 in progress | — | — |
| 2 | Topical group audit (5 opus agents) | ⏳ pending | `.work/audit/stage2-groups/*.md` | — |
| — | Correction Pass 2 (orchestrator edits) | ⏳ pending | — | — |
| 3 | Citation tracking (1 agent, edits survey) | ⏳ pending | `.work/audit/stage3-citations/report.md` | — |
| 4 | Citation verification (3 opus agents) | ⏳ pending | `.work/audit/stage4-verification/*.md` | — |
| — | Correction Pass 3 (orchestrator edits) | ⏳ pending | — | — |

## Stage 1 per-paper checklist

Each agent ticks its own row on completion. Status values: `⏳` pending, `🔄` running, `✅` done.

| # | PDF | Slug | Status | Artifact |
|---|-----|------|--------|----------|
| 1 | Aceto_2015_SAA_folium_orchil_diagnostic.pdf | aceto-2015 | ✅ | `.work/audit/stage1-per-paper/aceto-2015.md` |
| 2 | Aceto_2019_SAA_mythic_dyes_codices.pdf | aceto-2019 | ✅ | `.work/audit/stage1-per-paper/aceto-2019.md` |
| 3 | AchillesTatius_Leucippe_Clitophon_Loeb_L045.pdf | achilles-tatius | ✅ | `.work/audit/stage1-per-paper/achilles-tatius.md` |
| 4 | Ballard_2007_StudConserv_review_Cardon.pdf | ballard-2007 | ✅ | `.work/audit/stage1-per-paper/ballard-2007.md` |
| 5 | Beecken_1961_AngewChem_orcein_lackmus_German.pdf | beecken-1961 | ✅ | `.work/audit/stage1-per-paper/beecken-1961.md` |
| 6 | Beecken_2003_BiotechHistochem_orcein_litmus_English.pdf | beecken-2003 | ✅ | `.work/audit/stage1-per-paper/beecken-2003.md` |
| 7 | Bicchieri_2014_ESPR_Codex_Rossanensis.pdf | bicchieri-2014 | ✅ | `.work/audit/stage1-per-paper/bicchieri-2014.md` |
| 8 | Cala_2019_MicrochemJ_orchil_HPLC_MS.pdf | cala-2019 | ✅ | `.work/audit/stage1-per-paper/cala-2019.md` |
| 9 | Cassiodorus_Variae_Hodgkin_1886_IA.pdf | cassiodorus | ✅ | `.work/audit/stage1-per-paper/cassiodorus.md` |
| 10 | Clementi_2006_SAA_fluorimetry_orcein.pdf | clementi-2006 | ✅ | `.work/audit/stage1-per-paper/clementi-2006.md` |
| 11 | Dioscorides_DeMateriaMedica_Osbaldeston_2000.pdf | dioscorides | ✅ | `.work/audit/stage1-per-paper/dioscorides.md` |
| 12 | Doherty_2014_JRS_SERS_orchil_Roccella_Lasallia.pdf | doherty-2014 | ✅ | `.work/audit/stage1-per-paper/doherty-2014.md` |
| 13 | Ferreira_2004_ChemSocRev_natural_constituents_historical_dyes.pdf | ferreira-2004 | ✅ | `.work/audit/stage1-per-paper/ferreira-2004.md` |
| 14 | Frezza_2024_Pharmaceutics_Roccella_tinctoria.pdf | frezza-2024 | ✅ | `.work/audit/stage1-per-paper/frezza-2024.md` |
| 15 | Harborne_1997_Phytochemistry_review_Huneck_Yoshimura.pdf | harborne-1997 | ✅ | `.work/audit/stage1-per-paper/harborne-1997.md` |
| 16 | Hofmann_Aceto_2020_Vienna_Genesis_OAPEN.pdf | hofmann-aceto-2020 | ✅ | `.work/audit/stage1-per-paper/hofmann-aceto-2020.md` |
| 17 | Huneck_Yoshimura_1996_Springer_Identification_Lichen_Substances.pdf | huneck-yoshimura-1996 | ✅ | `.work/audit/stage1-per-paper/huneck-yoshimura-1996.md` |
| 18 | Jensen_2008_Leyden_Stockholm_papyri.pdf | jensen-2008 | ✅ | `.work/audit/stage1-per-paper/jensen-2008.md` |
| 19 | Kok_1966_Lichenologist_orchil_dyes_history.pdf | kok-1966 | ✅ | `.work/audit/stage1-per-paper/kok-1966.md` |
| 20 | Lackner_2024_Heritage_lichen_tapestry.pdf | lackner-2024 | ✅ | `.work/audit/stage1-per-paper/lackner-2024.md` |
| 21 | MoulheratSpantidaki_2011_PV3_Vindolanda_textiles.pdf | moulherat-spantidaki-2011 | ✅ | `.work/audit/stage1-per-paper/moulherat-spantidaki-2011.md` |
| 22 | Musso_1960_PlantaMed_orcein_lackmus.pdf | musso-1960 | ✅ | `.work/audit/stage1-per-paper/musso-1960.md` |
| 23 | Pliny_NH_Loeb_L353_books_8-11.pdf | pliny-l353 | ✅ | `.work/audit/stage1-per-paper/pliny-l353.md` |
| 24 | Pliny_NH_Loeb_L370_books_12-16.pdf | pliny-l370 | ✅ | `.work/audit/stage1-per-paper/pliny-l370.md` |
| 25 | Pliny_NH_Loeb_L392_books_20-23.pdf | pliny-l392 | ✅ | `.work/audit/stage1-per-paper/pliny-l392.md` |
| 26 | Pliny_NH_Loeb_L393_books_24-27.pdf | pliny-l393 | ✅ | `.work/audit/stage1-per-paper/pliny-l393.md` |
| 27 | Pliny_NH_Loeb_L394_books_33-35.pdf | pliny-l394 | ✅ | `.work/audit/stage1-per-paper/pliny-l394.md` |
| 28 | PseudoAristotle_De_Coloribus_Loeb_L307.pdf | pseudo-aristotle | ✅ | `.work/audit/stage1-per-paper/pseudo-aristotle.md` |
| 29 | Reinhold_1969_ClassicalJournal_status_symbols.pdf | reinhold-1969 | ✅ | `.work/audit/stage1-per-paper/reinhold-1969.md` |
| 30 | Roca_2026_SSRN_orcein_Part_B.pdf | roca-2026 | ✅ | `.work/audit/stage1-per-paper/roca-2026.md` |
| 31 | Sanyova_2008_DHA21_spectroscopic_studies_anthraquinone_aluminium_complexes.pdf | sanyova-2008 | ✅ | `.work/audit/stage1-per-paper/sanyova-2008.md` |
| 32 | Serafini_2018_MicrochemJ_orcein_lichen_species.pdf | serafini-2018 | ✅ | `.work/audit/stage1-per-paper/serafini-2018.md` |
| 33 | Smith_1921_Lichens_Cambridge_Botanical_Handbooks.pdf | smith-1921 | ✅ | `.work/audit/stage1-per-paper/smith-1921.md` |
| 34 | Tehler_2003_Taxon_Roccella_phycopsis.pdf | tehler-2003 | ✅ | `.work/audit/stage1-per-paper/tehler-2003.md` |
| 35 | Tehler_2009_SystBiodivers_American_Roccella.pdf | tehler-2009 | ✅ | `.work/audit/stage1-per-paper/tehler-2009.md` |
| 36 | TehlerIrestedt_2007_Cladistics_Roccellaceae_phylogeny.pdf | tehler-irestedt-2007 | ✅ | `.work/audit/stage1-per-paper/tehler-irestedt-2007.md` |
| 37 | Theophrastus_HP_Loeb_L70_books_1-5.pdf | theophrastus-l70 | ✅ | `.work/audit/stage1-per-paper/theophrastus-l70.md` |
| 38 | Theophrastus_HP_Loeb_L79_books_6-9.pdf | theophrastus-l79 | ✅ | `.work/audit/stage1-per-paper/theophrastus-l79.md` |
| 39 | VerheckenLammens_2010_ATN51_Roman_tunics_purple.pdf | verhecken-lammens-2010 | ✅ | `.work/audit/stage1-per-paper/verhecken-lammens-2010.md` |
| 40 | Vitruvius_Granger_Loeb_L251_L280_complete.pdf | vitruvius | ✅ | `.work/audit/stage1-per-paper/vitruvius.md` |
| 41 | Wainwright_2003_BiotechHistochem_orcein_revealed.pdf | wainwright-2003 | ✅ | `.work/audit/stage1-per-paper/wainwright-2003.md` |
| 42 | WaltonTaylor_1983_TextileHistory_Vindolanda_dyes.pdf | walton-taylor-1983 | ✅ | `.work/audit/stage1-per-paper/walton-taylor-1983.md` |
| 43 | Whitworth_2025_Heritage_milking_orchil.pdf | whitworth-2025 | ✅ | `.work/audit/stage1-per-paper/whitworth-2025.md` |
| 44 | Whitworth_Koren_2016_Ambix_Bedfords_Leeds.pdf | whitworth-koren-2016 | ✅ | `.work/audit/stage1-per-paper/whitworth-koren-2016.md` |
| 45 | Witkowski_2017_MicrochemJ_orcein_liturgical_paraments.pdf | witkowski-2017 | ✅ | `.work/audit/stage1-per-paper/witkowski-2017.md` |
| 46 | Wouters_2008_DHA21_Roman_Eastern_Desert_dyes.pdf | wouters-2008 | ✅ | `.work/audit/stage1-per-paper/wouters-2008.md` |

## Error tallies

_Filled as stages complete._

- Stage 1 misattributions: —
- Stage 1 fabricated / unsupported claims: —
- Stage 1 wrong numbers / samples / dates: —
- Stage 1 omissions flagged (primer-scope calibrated): —
- Stage 2 cross-paper inconsistencies: —
- Stage 3 claims added citations for / unsourceable: — / —
- Stage 4 Verified / Partial / Unsupported / Unverifiable: — / — / — / —

## Commit log

_Updated after each correction pass._
