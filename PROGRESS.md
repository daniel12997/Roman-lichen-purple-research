# Progress — Roman Lichen Purple Research

**Topic:** **Lichen-derived purple dyes (orchil) in the Roman Empire and adjacent periods.** Shellfish/Tyrian purple appears only as context (the thing orchil imitates).
**Scope change:** originally framed as all Roman purple dyes; rescoped 2026-04-22 to lichen-specific, and repo renamed from `Roman-purple-dye-research` to `Roman-lichen-purple-research`.
**Reference model:** `/home/daniel-parker/repos/Waring-states-bead-research/warring_states_beads_resources.md`
**Target file:** `roman_lichen_purple_dye_resources.md` (to be drafted by Stage 5b).
**Broader-scope draft (superseded):** `.work/broader-draft.md` — 627 lines; retained as reference.
**Scratch dir:** `.work/` (gitignore before final commit).
**PDF dir:** `research_documents/`.

## Pipeline status

| # | Stage | Status | Artifact |
|---|-------|--------|----------|
| 1 | Topic-split research (4 agents: archaeometric / historical / lichen-bio / chronology) | ✅ complete | dispatched pre-artifact-pattern; outputs inline, now folded into Stage 2 |
| 2 | Dedupe master list | ✅ complete | `.work/stage2/master-list.md` (90 unique entries) |
| 3 | Download open-access PDFs | ✅ complete | 29 PDFs in `research_documents/`, `INDEX.md` + `.work/stage3/download-manifest.md` |
| 4 | Per-paper summaries (Haiku #1–48, Sonnet #49–86) | ✅ complete — 86 per-paper summary files in `.work/stage4/` | `.work/stage4/<slug>.md` |
| 5a | Broader-scope assembly (superseded) | ✅ complete; output moved to `.work/broader-draft.md` | — |
| 5b | Lichen-focused assembly | ✅ complete — 413 lines | `roman_lichen_purple_dye_resources.md` |

## Stage 3 access-route notes

- PMC proof-of-work interstitial blocks curl for Cooksey 2013 and Vienna Genesis article → Vienna Genesis pivoted to full CC-BY OAPEN book via IA mirror.
- HAL-SHS, OpenEdition use Anubis JS challenge → Wouters 2008 and Wild 2005 landing-page-only.
- Academia.edu, ResearchGate, SSRN, T&F all Cloudflare-gated for curl (incl. the "T&F Open" Shalvi 2023) → landing-page-only.
- Edelstein Center WordPress hosts author-mirror PDFs for several paywalled Koren papers → used for #10, #17, #18, #52.
- Loeb: Pliny/Vitruvius older volumes on IA; Aristotle LCL 437 is IA-borrow-only.
- ~29 downloaded / 61 paywall-or-book-or-skipped.

## Orchestration rules (user-specified)

- Main loop is **orchestrator only** — no WebSearch/WebFetch/content authorship in-loop.
- All agents run **in the background** (`run_in_background: true`).
- Agents produce **file artifacts**, not inline returns. Downstream agents read the files.
- Stage 4 per-paper summary agents use **model: haiku**, capped at **10 concurrent**, batched.
- Summaries must include **(a) 1–3 sentence summary + (b) key technical terms** with glosses where non-obvious.

## Decisions log

- **Scope (original):** broader — covered murex Tyrian, lichen orchil, and imitation purples together.
- **Scope (2026-04-22 revision):** narrowed to **lichen/orchil** specifically. Shellfish purple retained only as context (what orchil imitates). Most shellfish-only papers are dropped from the final document; their stage4 summaries remain in `.work/stage4/` and are fully represented in the superseded broader draft.
- **Axes for research split:** A archaeometric / B historical-legal / C lichen-bio / D chronology & case studies. (The Agent C corpus is now the primary source for the lichen-focused document.)
- **Download before summarize** so per-paper agents read full text when available → higher-accuracy summaries.
- **Stage 5 split:** 5a broader draft (completed, archived in `.work/broader-draft.md`), 5b lichen-focused (in flight).

## Stage 2 key resolutions (from dedup agent)

- **Papliaka / Konstanta / Karapanagiotis et al. 2017** — corrects Agent A's mis-attribution to Rosenberg et al. (FTIR+HPLC on molluskan purple).
- **Shalvi & Gilboa et al. 2023** — corrects the Tel Aviv 50(1):3–40 authorship (not Shaer, not Gilboa-first; Shalvi is lead).
- **Calà et al. 2019** — article ID 104081 is correct (104140 was a typo from one agent).
- **Zaffino 2016 vs Witkowski 2017** — two different papers with near-identical titles; both retained.
- **Serafini et al. 2018** absorbs Agent A's mis-cited "Zaffino 2017"; same paper.

## Outstanding conflicts (for later verification)

- **Aceto et al. 2020 Vienna Genesis** — full venue split between book chapter and journal article still needs verification at download time.
- **Koren Masada** — 1994 IES chapter and 1997 AIC postprint kept separately (may be duplicates in spirit; resolve at Stage 5).

## Source counts

- **Raw:** ~108 across four agents
- **Unique:** 90 master-list entries + subseries splits
- **Open-access PDFs targetable:** ~20 (MDPI Heritage/Molecules/Sustainability/Pharmaceutics, PLOS ONE, PMC mirrors, HAL, Academia, arXiv preprint, Project Gutenberg)
- **Paywalled:** ~60 (T&F, Elsevier, Wiley, Springer, SAGE, De Gruyter) — abstract/publisher-page fallback for Stage 4
- **Books / library-only:** ~10 (Reinhold, Cardon, Spanier, Longo, Harlow & Nosch, Purpureae Vestes series, Loeb volumes, etc.)

## Artifacts

- Reference file (read-only): `../Waring-states-bead-research/warring_states_beads_resources.md`
- Stage 2 output: `.work/stage2/master-list.md`
- Stage 3 output (pending): `research_documents/INDEX.md`, `.work/stage3/download-manifest.md`
- Stage 4 output (pending): `.work/stage4/*.md`
- Stage 5a output (archived): `.work/broader-draft.md`
- Stage 5b output: `roman_lichen_purple_dye_resources.md` (413 lines)
- Post-rescope archive: `.work/shellfish-context/` — 17 scope-adjacent PDFs moved out of `research_documents/` on 2026-04-22. `research_documents/INDEX.md` regenerated to reflect lichen-only scope + pointer to archive.
- Stage 6 deep-search output: `.work/stage6/deep-search-report.md` — attempted IRIS/ORA/DiVA/Meise/Unpaywall/preprint retrieval for the 24 paywalled lichen papers. **Result: 1 new PDF (Aceto 2015 from IRIS UniTO), 23 still unavailable.** Cloudflare Turnstile blocks Wiley / T&F / ResearchGate / SSRN from this IP even with Playwright.

## Stage 6 findings to propagate

**Three DOI errors discovered in the master list, need patching in the final deliverable and master-list:**
1. **Calà et al. 2019** — correct DOI is `10.1016/j.microc.2019.104140`, not `104081` (104081 resolves to an unrelated Argentine PAH paper)
2. **Aceto et al. 2019 "Mythic Dyes"** — correct DOI is `10.1016/j.saa.2019.01.091`, not `10.1016/j.saa.2018.11.027` (latter resolves to a ZnS quantum-dot paper)
3. **Zaffino, Russo, Bruni 2016** — DOI `10.1016/j.microc.2016.10.020` resolves to an unrelated Argentine PAH paper. CrossRef author search found **no Zaffino + orcein paper in Microchem. J. vol. 131**. Likely a citation error from the original research agents; may be a hallucinated source. Needs human verification or removal.

**Ferreira 2004 mismatch confirmed** — Glasgow Enlighten record 109139 itself has the wrong PDF attached (Hulme et al. flavonoid conference proceedings). The Chem. Soc. Rev. review has no known open copy.

**Tehler & Irestedt 2007** — confirmed OA via Unpaywall, but our IP is Cloudflare-blocked from Wiley. User could fetch from a residential or academic network.

## Skill

Workflow encoded at `~/.claude/skills/research-bibliography/SKILL.md` for reuse on future topics.
