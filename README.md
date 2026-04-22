# Roman Lichen Purple (Orchil) Dye — Annotated Research Bibliography

Lichen-derived purple dye (orchil) in the Roman Empire and adjacent late-antique periods: a pointer list to published sources with per-entry critical annotation.

---

## Topic overview

Orchil is a purple-red textile dye produced from *Roccella* and related lichens by ammonia fermentation, which converts colourless orcinol-class depsides to a complex mixture of phenoxazone chromophores (orcein). In the Roman world it served as a cheaper, more accessible substitute for shellfish-derived Tyrian purple — and, recent analytical work has shown, as the actual purple used on late-antique parchment codices long assumed to be murex-dyed. The question of whether Greek and Latin authors (*phycos thalassion* in Dioscorides; *phycos* in Pliny NH 13 and 26) were describing a *Roccella*-type lichen or a true alga remains the central philological problem, with the *Roccella* identification proposed by Kok (1966) and Smith (1921) but not yet resolved by direct textual audit.

---

## What this is / what this isn't

> **What this is:** a pointer list to published sources on lichen-derived purple dye (orchil) in the Roman and late-antique world — primary analytical chemistry, reference volumes, lichen taxonomy, ethnobotanical analogues, ancient texts, and Roman-period case studies where orchil has been chemically identified. Each entry is meant to help you decide whether to open the source and what to look for when you do.
>
> **What this isn't:** a general history of Roman purple, and it is not a research artifact to be cited directly. Shellfish (Tyrian/murex) purple appears here only as context — it is what orchil imitated, competed with, and was sometimes used to adulterate. The "Summary of Key Findings" at the bottom is rough orientation; trace any claim back to its cited paper before citing elsewhere.

---

## Repo layout

```
roman_lichen_purple_dye_resources.md   Main deliverable — annotated bibliography
                                        (~420 lines; 23 sources + glossary +
                                        summary of key findings)

research_documents/                    23 open-access PDFs:
                                        - 13 secondary literature papers
                                        - 10 ancient primary texts
                                          (Loeb Pliny vols. L353, L370, L392, L393;
                                           Theophrastus L79; Jensen 2008 Leyden/
                                           Stockholm papyri; Pseudo-Aristotle L307;
                                           Vitruvius L280; Cassiodorus Hodgkin;
                                           Dioscorides Osbaldeston)

research_documents/INDEX.md            Catalogue of all 23 downloaded PDFs with
                                        source URLs and access notes, plus the full
                                        "Not Downloaded" table of paywalled citations
                                        and archived scope-adjacent items

PROGRESS.md                            5-stage build pipeline log: topic-split
                                        research → dedup → PDF download → per-paper
                                        summaries → final assembly; scope-change
                                        history; orchestration decisions

AUDIT_PROGRESS.md                      4-stage audit pipeline: per-paper fact-check
                                        (13 Sonnet agents) → topical group audit →
                                        citation tracking → citation verification;
                                        3 correction passes between stages

.work/                                 Pipeline scratch — gitignored
                                        stage2/   deduplicated master list (90 entries)
                                        stage3/   download manifest
                                        stage4/   86 per-paper summary files (Haiku)
                                        stage6/   deep-search report for paywalled items
                                        stage8/   primary-source full-text report
                                        stage9-audit/  per-paper fact-check artifacts
                                        broader-draft.md  superseded 627-line draft
                                        shellfish-context/  17 scope-adjacent PDFs
                                                            moved out during rescope

.gitattributes                         Git LFS tracking for the two >100 MB Pliny
                                        volumes (L392 and L393)
```

---

## Known limitations

These should be checked before citing.

- **Four load-bearing papers remain paywalled** and were summarized from abstracts only: Walton/Taylor 1983 (*Textile History* 14(2):115–124 — the foundational Roman textile identification at Vindolanda); Moulherat & Spantidaki 2011 (*Purpureae Vestes III*); Aceto et al. 2019 "Mythic Dyes" (*Spectrochim. Acta A* 215:133–141); Wouters et al. 2008 (*Dyes in History and Archaeology* 21:1–16).
- **Theophrastus L79 file mislabeled:** `Theophrastus_HP_Loeb_L79_books_4-5.pdf` actually contains Books VI–IX. HP 4.6.5 (the *phycos* passage) cannot be verified from this corpus; re-download of the correct volume is needed.
- **Ferreira 2004 wrong file:** the local PDF `Ferreira_2004_ChemSocRev_natural_constituents_historical_dyes.pdf` is a Hulme et al. flavonoid conference paper, not the *Chemical Society Reviews* article. The CSR text has no confirmed open-access copy; do not cite the local file as Ferreira 2004.
- **Roca et al. 2026** is an SSRN preprint, not yet peer-reviewed.
- Kok (1966) and Smith (1921) are paywalled; the *Roccella* identification of Pliny's *phycos* therefore rests on secondary literature, not direct audit of those texts, within this corpus.

---

## How it was built

The bibliography was compiled through an orchestration-only subagent pipeline. Stage 1 dispatched four parallel research agents (archaeometric / historical / lichen-biology / chronology axes), producing ~108 raw source candidates. Stage 2 deduplicated these to a 90-entry master list. Stage 3 downloaded open-access PDFs via Internet Archive, MDPI, OAPEN, arXiv, Edelstein Center mirrors, and IRIS UniTO AperTO bitstreams; a Stage 6 deep-search pass added one further paper (Aceto 2015 from IRIS). Stage 4 ran 86 per-paper summary agents (Haiku, batched at ≤10 concurrent) across downloaded PDFs and publisher abstracts. Stage 5 assembled the lichen-focused deliverable; a broader-scope draft was archived in `.work/`. The audit pipeline (AUDIT_PROGRESS.md) ran 13 Sonnet per-paper fact-check agents, followed by topical group audits, citation tracking, and citation verification, with compiler-driven correction passes between each stage.

The `research-bibliography` and `research-survey-audit` skills that encode this workflow are at `~/.claude/skills/` and are reusable for other topics.

---

## Cloning — Git LFS note

Two Pliny volumes exceed 100 MB and are tracked via Git LFS (see `.gitattributes`):

- `research_documents/Pliny_NH_Loeb_L392_books_20-23.pdf`
- `research_documents/Pliny_NH_Loeb_L393_books_24-27.pdf`

Without LFS, you will get pointer files rather than the actual PDFs. To clone with full content:

```bash
git lfs install
git clone https://github.com/daniel12997/Roman-lichen-purple-research
```

Or, after a plain clone:

```bash
git lfs pull
```

---

## Attribution / licensing

`roman_lichen_purple_dye_resources.md` is original compilation work by Daniel Parker. The PDFs in `research_documents/` are third-party works under their respective licenses: MDPI CC BY (Lackner 2024; Frezza 2024; Whitworth 2025); OAPEN CC BY 4.0 (Hofmann/Aceto 2020 Vienna Genesis book); arXiv preprint (Bicchieri 2014); IRIS UniTO AperTO preprint (Aceto 2015); Edelstein Center author mirror (Whitworth & Koren 2016); Internet Archive public-domain Loeb scans (Pliny L353, L370, L392, L393; Theophrastus L79; Pseudo-Aristotle L307; Vitruvius L280; Cassiodorus Hodgkin 1886); Internet Archive / Project Gutenberg (Smith 1921); Internet Archive (Dioscorides Osbaldeston 2000; Jensen 2008 Leyden/Stockholm papyri); journal open-access (Reinhold 1969; ATN 51 / Verhecken-Lammens 2010). See `research_documents/INDEX.md` for per-file access routes.
