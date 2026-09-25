# CLAUDE.MD -- Empirical Economics Research with Claude Code

<!-- HOW TO USE: Replace [BRACKETED PLACEHOLDERS] with your project info.
     Customize Beamer environments for your talk preamble.
     Keep this file under ~150 lines — Claude loads it every session.
     See the guide at https://hugosantanna.github.io/clo-author/ for full documentation. -->

**Project:** [YOUR PROJECT NAME]
**Institution:** [YOUR INSTITUTION]
**Field:** [YOUR FIELD — Economics by default. Can be adapted to Finance, Accounting, Marketing, etc.]
**Branch:** main

---

## Core Principles

- **Plan first** -- enter plan mode before non-trivial tasks; save plans to `quality_reports/plans/`
- **Verify after** -- compile and confirm output at the end of every task
- **Single source of truth** -- Paper `main.tex` is authoritative; talks and supplements derive from it
- **Quality gates** -- weighted aggregate score; nothing ships below 80/100; see `quality.md`
- **Worker-critic pairs** -- every creator has a paired critic; critics never edit files
- **Auto-memory** -- corrections and preferences are saved automatically via Claude Code's built-in memory system
- **Two-layer writing policy** -- Scientific Style governs evidence/argument; Elite Economics Voice governs high-quality prose realization

---

## Getting Started

1. Fill in the `[BRACKETED PLACEHOLDERS]` in this file
2. Run `/discover interview [topic]` to build your research specification
3. Or run `/new-project [topic]` for the full orchestrated pipeline

---

## Folder Structure

```
[YOUR-PROJECT]/
├── CLAUDE.MD                    # This file
├── .claude/                     # Rules, skills, agents, hooks
│   └── references/
│       ├── style-bundle/        # Distilled scientific/rhetorical policy
│       └── elite-econ-voice/    # Elite empirical-economics prose realization
├── Bibliography_base.bib        # Centralized bibliography
├── paper/                       # Main LaTeX manuscript (source of truth)
│   ├── main.tex                 # Primary paper file
│   ├── sections/                # Section-level .tex files
│   ├── figures/                 # Generated figures (.pdf, .png)
│   ├── tables/                  # Generated tables (.tex)
│   ├── talks/                   # Beamer presentations
│   ├── quarto/                  # Quarto RevealJS presentations
│   ├── preambles/               # LaTeX headers / shared preamble
│   ├── supplementary/           # Online appendix and supplements
│   └── replication/             # Replication package for deposit
├── data/                        # Project data
│   ├── raw/                     # Original untouched data (often gitignored)
│   └── cleaned/                 # Processed datasets ready for analysis
├── scripts/                     # Analysis code (R, Python, Julia)
├── quality_reports/             # Plans, session logs, reviews, scores
├── explorations/                # Research sandbox (see rules)
├── templates/                   # Session log, quality report templates
└── master_supporting_docs/      # Reference papers and data docs
```

---

## Writing Style Integration

Clo-Author uses two separate corpus-derived layers.

### Layer 1 — Distilled Scientific Style

Active when `.claude/references/style-bundle/STYLE_SPEC.md` exists.

Load:
1. `STYLE_MANIFEST.md`
2. relevant rule IDs from `STYLE_SPEC.md`
3. `CLAIM_EVIDENCE_RULES.md`
4. target-section grammar from `SECTION_GRAMMARS.md`
5. relevant anti-patterns/checks

This layer governs claim strength, evidence order, rhetorical architecture, mechanism language, robustness logic, and section discipline.

### Layer 2 — Elite Economics Voice

Active when `.claude/references/elite-econ-voice/VOICE_SPEC.md` exists.

Load:
1. `VOICE_MANIFEST.md`
2. target-section EV-SIG / EV-DEF / EV-AVOID rules from `VOICE_SPEC.md`
3. relevant move realization, hedging, rhythm, transition, and citation resources
4. `VOICE_CRITIC_CHECKS.md` for preflight/review

This layer governs linguistic realization: research-agent syntax, verb choice, magnitude integration, contrasts, local hedging, clause order, transitions, citation voice, and paragraph rhythm. It must never strengthen a claim beyond the Scientific Style permission.

### Optional Personal Voice

`.claude/references/personal-style-guide.md` is a lower-priority optional overlay. When Elite Economics Voice is active, personal voice is **opt-in**: do not load, apply, or score it unless the user/project explicitly enables personal-voice matching.

Conflict precedence:

**verified evidence/results > content invariants/identification > Scientific Style claim-evidence + HARD rules > working-paper format > Scientific Style strong defaults/section grammar > Elite Voice EV-SIG > Elite Voice EV-DEF > personal voice > optional styles/examples > generic templates.**

Never imitate recognizable wording or signature phrases from any source scholar. The Elite Voice layer transfers ensemble writing mechanisms, not author identity.

---

## Commands

```bash
# Paper compilation (latexmk handles multi-pass + biber automatically)
cd paper && latexmk main.tex

# Talk compilation
cd paper/talks && latexmk talk.tex

# Clean auxiliary files
cd paper && latexmk -c
```

> **Note:** `paper/latexmkrc` configures XeLaTeX, TEXINPUTS, and BIBINPUTS.
> On Overleaf, set compiler to XeLaTeX via Menu > Compiler — Overleaf reads `latexmkrc` automatically.

---

## Quality Thresholds

| Score | Gate | Applies To |
|-------|------|------------|
| 80 | Commit | Weighted aggregate (blocking) |
| 90 | PR | Weighted aggregate (blocking) |
| 95 | Submission | Aggregate + all components >= 80 |
| -- | Advisory | Talks (reported, non-blocking) |

See `quality.md` for weighted aggregation formula.

---

## Skills Quick Reference

| Command | What It Does |
|---------|-------------|
| `/new-project [topic]` | Full pipeline: idea → paper (orchestrated) |
| `/discover [mode] [topic]` | Discovery: interview, literature, data, ideation |
| `/strategize [mode] [question]` | Identification strategy, pre-analysis plan, or formal theory section (`theory` mode) |
| `/analyze [dataset]` | End-to-end data analysis |
| `/write [section]` | Draft using Scientific Style + Elite Economics Voice; personal voice is optional and lower-priority |
| `/review [file/--flag]` | Quality reviews (routes by target: paper, code, peer) |
| `/revise [report]` | R&R cycle: classify + route referee comments |
| `/talk [mode] [format]` | Create, audit, or compile Beamer presentations |
| `/submit [mode]` | Journal targeting → package → audit → final gate |
| `/tools [subcommand]` | Utilities: commit, compile, validate-bib, journal, etc. |
| `/checkpoint [--flag]` | Session handoff: memory + SESSION_REPORT + research journal (+ Obsidian if configured) |

---

<!-- CUSTOMIZE: Replace the example entries below with your own
     Beamer environments for talks. -->

## Beamer Custom Environments (Talks)

| Environment       | Effect        | Use Case       |
|-------------------|---------------|----------------|
| `[your-env]`      | [Description] | [When to use]  |

---

## Output Organization

<!-- Options: by-script (default) or by-purpose -->
Output organization: by-script

<!-- by-script:  paper/figures/main_regression/figure1.pdf, paper/tables/main_regression/table1.tex -->
<!-- by-purpose: paper/figures/estimation/coefplot_main.pdf, paper/tables/robustness/alt_controls.tex -->

---

## Current Project State

| Component | File | Status | Description |
|-----------|------|--------|-------------|
| Paper | `paper/main.tex` | [draft/submitted/R&R] | [Brief description] |
| Data | `scripts/R/` | [complete/in-progress] | [Analysis description] |
| Replication | `paper/replication/` | [not started/ready] | [Deposit status] |
| Job Market Talk | `paper/talks/job_market_talk.tex` | -- | [Status] |
