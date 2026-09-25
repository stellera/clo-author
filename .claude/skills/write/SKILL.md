---
name: write
description: Draft academic paper sections using paragraph-level argument moves. Cleanup pass strips AI patterns after drafting. Replaces /draft-paper and /humanizer.
argument-hint: "[section or mode: intro | strategy | results | conclusion | abstract | full | humanize | style-guide] [file path (optional)]"
allowed-tools: Read,Grep,Glob,Write,Edit,Task
---

# Write

Draft paper sections, apply a cleanup pass, or extract a personal style guide from prior papers by dispatching the **Writer** agent.

**Input:** `$ARGUMENTS` — section name or mode, optionally followed by file path.

---

## Modes

### `/write [section]` — Draft Paper Section
Draft a specific section: `intro`, `strategy`, `results`, `conclusion`, `abstract`, or `full`.

**Agent:** Writer
**Output:** LaTeX section file in paper/sections/

Workflow:

#### 1. Context Gathering

Before drafting, read all available context:
1. Read existing paper draft in `paper/` (if it exists)
2. Read `master_supporting_docs/` for notes, outlines, research specs
3. Read most recent `quality_reports/research_spec_*.md` or `quality_reports/lit_review_*.md`
4. Read `.claude/references/domain-profile.md` for field conventions
5. Check `Bibliography_base.bib` for available citations
6. Scan `paper/tables/` and `paper/figures/` for generated output
7. Read `quality_reports/results_summary.md` if it exists (from Coder)
8. Check `.claude/references/style-bundle/STYLE_SPEC.json`. If present, validate the required Style Bundle files and load the bundle according to the Writer's Style Calibration Stack.
9. For an active bundle, load global HARD_RULES, `CLAIM_EVIDENCE_RULES.md`, `FORBIDDEN_PATTERNS.md`, and only the target section's relevant material from `SECTION_GRAMMARS.md`. Load `STYLE_EXAMPLES.md` only when examples are needed.
10. Read `.claude/references/personal-style-guide.md` if it contains real extracted content. Personal voice is optional when a valid Distilled Style Bundle is active.

#### 2. Paper Type Detection

Before routing, identify the paper type from the strategy memo or existing draft:
- **Reduced-form** — DiD, IV, RDD, event study
- **Structural** — Model estimation, counterfactual simulations
- **Theory + empirics** — Propositions tested with data
- **Descriptive / measurement** — New data, new measure, stylized facts

This determines which section templates the Writer uses.

#### 3. Section Routing

Based on `$ARGUMENTS`:
- **`full`**: Draft all sections in sequence, pausing between major sections for user feedback
- **`intro`**: Draft introduction (most common request)
- **`strategy`**: Draft empirical strategy (reduced-form), model + estimation (structural), or model + tests (theory+empirics)
- **`results`**: Draft results — narration style depends on paper type and output type (regression tables, event study figures, counterfactual simulations, etc.)
- **`conclusion`**: Draft conclusion with type-appropriate ending (policy implications, counterfactual implications, or research agenda)
- **`abstract`**: Draft abstract (must have other sections first)
- **`data`**: Draft data section — expanded for descriptive/measurement papers
- **`model`**: Draft model section (structural or theory+empirics papers only)
- **No argument**: Ask user which section to draft

#### 4. Dispatch Writer

Dispatch Writer with the paper type, the active Style Calibration Stack, and the target section's argument-move resources.

If a valid Distilled Style Bundle is active, corpus-derived HARD_RULES and section grammar take precedence over generic Clo-Author templates where they overlap. Generic templates remain fallbacks where the bundle is silent. Personal style, when available, calibrates voice within those constraints.

The writer drafts using one primary argumentative job per paragraph, applies design-specific moves and claim-evidence calibration, then runs the cleanup pass against both generic cleanup patterns and the distilled `FORBIDDEN_PATTERNS.md`. Save to `paper/sections/[section].tex`.

#### 5. Quality Self-Check

Before presenting the draft:
- [ ] Paper type identified and correct template used
- [ ] Every paragraph has an identifiable purpose (argument move type)
- [ ] Findings lead sentences — not buried after setup
- [ ] Design-specific elements present (see writer.md for checklists per design)
- [ ] Every displayed equation is numbered (`\label{eq:...}`)
- [ ] All `\cite{}` keys exist in `Bibliography_base.bib`
- [ ] Introduction contribution paragraph names specific papers
- [ ] Effect sizes stated with units
- [ ] No banned hedging phrases
- [ ] Notation consistent throughout
- [ ] All tables/figures referenced actually exist in `paper/tables/` or `paper/figures/`
- [ ] Results narrated correctly for output type (tables, event study figures, counterfactuals)
- [ ] Style calibration available: valid Distilled Style Bundle and/or populated personal style guide
- [ ] If Distilled Style Bundle is active, target-section grammar and claim-evidence rules were applied
- [ ] If Distilled Style Bundle is active, no HARD_RULE or distilled forbidden-pattern violations remain
- [ ] Claim-source map produced for all numerical claims (`quality_reports/claim_source_map_{project}.md`)
- [ ] Results/Conclusion only drafted after verifying actual output files exist

#### 6. Present to User

Present sections through drafting gates, pausing for approval at each:

**GATE 1:** Introduction + Literature positioning → present, wait for approval
**GATE 2:** Data + Empirical Strategy (or Model) → present, wait for approval
**GATE 3:** Results + Robustness + Conclusion → present, wait for approval

For single-section drafts, present the section directly. For `full`, use all three gates.

Flag items that need attention:
- **BLOCKED items:** Results/Conclusion cannot be drafted without output files
- **VERIFY items:** Citations that need user confirmation
- **STYLE items:** Distilled Style Bundle exists but is incomplete or inconsistent
- **VOICE items:** No valid Distilled Style Bundle and personal style guide is still a template (drafting blocked until one calibration source is available)

### `/write style-guide [paper-dir]` — Extract Personal Voice

One-shot extraction of the user's **personal writing voice** from their published or drafted papers. Produces `.claude/references/personal-style-guide.md`, which the writer auto-loads on subsequent invocations.

This mode is intentionally separate from the Distilled Style Bundle. It does not create, replace, or modify `.claude/references/style-bundle/`.

**When to run:**
- Once at the start of a project, after pointing at a directory of the user's prior papers
- After publishing a new paper that shifts voice (re-run to refresh the profile)

**Input:** `$ARGUMENTS` — path to a directory containing prior papers (.tex or .pdf). If omitted, defaults to `master_supporting_docs/` and scans for .tex/.pdf files.

**Agent:** Writer (style-extraction mode)
**Output:** `.claude/references/personal-style-guide.md`

Workflow:
1. **Discover corpus.** List .tex and .pdf files in the target directory. If fewer than 2 papers found, flag and ask before proceeding (style extraction on a single paper overfits).
2. **Sample strategically.** For each paper, extract:
   - The full introduction
   - The first two paragraphs of each major section
   - The abstract and conclusion
   - A random sample of 5–10 results-section paragraphs
   This keeps context usage bounded while capturing voice variation across sections.
3. **Extract patterns.** The Writer (in style-extraction mode) produces quantitative and qualitative patterns:
   - Sentence-length distribution (median, 10th–90th pct)
   - Passive-voice frequency, first-person-plural frequency, em dash rate
   - Paragraph opening and closing moves
   - Section-architecture patterns (how introductions open, how results lead)
   - Lexicon: words used repeatedly, words demonstrably avoided
   - Hedging and comparison patterns
   - Citation conventions (textual vs. parenthetical split; papers-per-claim)
   - Tone markers and anti-patterns already stripped
4. **Write to `.claude/references/personal-style-guide.md`.** Fill every template section with quoted examples from the corpus. Never invent patterns — if a section has no evidence, write "[insufficient corpus evidence]".
5. **Present summary.** One-paragraph recap of the voice profile: sentence length, passive rate, signature lexicon, distinguishing tone markers. User confirms before the guide takes effect on subsequent `/write` calls.

Principles for the extraction:
- **Ground every claim in the corpus.** Each pattern must have at least one quoted example.
- **Extract, don't prescribe.** The guide records the author's observed behavior, not what the Writer thinks is good style.
- **Don't duplicate `domain-profile.md`.** The style guide is about voice; the domain profile is about field conventions.
- **Don't override working-paper-format invariants.** Voice doesn't trump INV-1..21.
- **Don't override the Distilled Style Bundle.** When both are active, personal voice chooses among permitted variants but cannot override claim-evidence rules or distilled HARD_RULES.

### `/write humanize [file]` — Cleanup Pass Only
Strip AI writing patterns from existing text without rewriting content.

**Agent:** Writer (cleanup mode)
**Output:** Edited file with AI patterns removed

Strips 24 patterns across 4 categories:
- Structural: forced narrative arcs, artificial progression
- Lexical: "delve, leverage, nuanced, robust"
- Rhetorical: rule-of-three, negative parallelisms, em dash overuse
- Formatting: excessive bullet points, promotional language

---

## Section Standards

**All paper types share the same backbone. Moves diverge by type — see writer.md for full templates.**

| Section | Length | Reduced-Form | Structural | Theory+Empirics | Descriptive |
|---------|--------|-------------|-----------|----------------|-------------|
| Introduction | 1000-1500 | ...preview → result → contribution | ...model preview → counterfactual → contribution | ...theory preview → test result → contribution | ...data innovation → key fact → contribution |
| Data | 800-1200 | Treatment, outcome, controls | Moments that identify parameters | Standard | 1200-1800 (core contribution) |
| Strategy/Model | 800-1500 | Design-specific (DiD/IV/RDD/ES) | Environment → decisions → equilibrium → estimation | Model → propositions → tests | N/A (merged into Data) |
| Results | 800-1500 | Main spec → robustness → heterogeneity | Estimates → model fit → counterfactuals → welfare | Prediction-by-prediction evidence | Key facts → decompositions → implications |
| Conclusion | 500-700 | Policy implications | Counterfactual implications + model limitations | What model gets right/wrong | Research agenda enabled by new data |
| Abstract | 100-150 | Question, design, finding with magnitude | Question, model, counterfactual finding | Question, prediction, test result | Question, measurement, key fact |

---

## LaTeX Conventions

- `\citet{}` for textual citations ("Smith (2024) shows...")
- `\citep{}` for parenthetical citations ("...is well documented (Smith, 2024)")
- `booktabs` rules (`\toprule`, `\midrule`, `\bottomrule`) — never `\hline`
- Notation protocol: `Y_{it}`, `D_{it}`, `\gamma_i`, `\delta_t`, `\varepsilon_{it}`

---

## Bundled Resources (Level 3)

Loaded on demand by the writer agent:

| Resource | Path | When |
|----------|------|------|
| Section templates | `templates/section-templates.md` | Always -- defines section structure |
| Paragraph moves | `templates/paragraph-moves.md` | Always -- defines argument types |
| Cleanup patterns | `templates/cleanup-patterns.md` | After drafting -- cleanup pass |
| Style extraction | `templates/style-extraction-protocol.md` | `/write style-guide` mode |
| Drafting gates | `templates/drafting-gates.md` | Full draft mode |
| Claim-source map | `templates/claim-source-map.md` | After results section |
| Notation protocol | `references/notation-protocol.md` | Strategy + results sections |
| Distilled Style Bundle | `.claude/references/style-bundle/` | Drafting/revision when `STYLE_SPEC.json` is present |

See also: `gotchas.md` for known failure points and edge cases.

---

## Principles
- **This is the user's paper, not Claude's.** Use personal voice when available; otherwise use the validated Distilled Style Bundle rather than generic stylistic imitation.
- **Never fabricate results.** Use TBD placeholders.
- **Citations must be verifiable.** Only cite confirmed papers.
- **Argument moves first, cleanup second.** Draft with structure, then strip AI patterns.
