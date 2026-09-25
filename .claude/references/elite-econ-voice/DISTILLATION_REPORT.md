# Elite Economics Voice Distillation Report

## Goal

This distillation extracts transferable prose habits from a balanced corpus of 30 papers associated with Daron Acemoglu, Raj Chetty, Hanming Fang, Nancy Qian, Shaoda Wang, and David Y. Yang.

It does **not** create an impersonation layer. It deliberately excludes signature phrases, topic vocabulary, and wording that would make a draft sound like a particular living author. The output is an ensemble policy for clear empirical-economics prose.

## Corpus design

- 30 distinct papers, 5 per focal author.
- Equal author weighting and equal within-author paper weighting.
- Papers span AER, QJE, JPE, Review of Economic Studies, Journal of Public Economics, AEJ: Applied Economics, Review of Economics and Statistics, and NBER working-paper versions.
- Time coverage runs from classic early-2000s work to 2025–2026 publications/drafts.

See `CORPUS_MANIFEST.md` for the locked corpus.

## Evidence collected

The public-source environment is heterogeneous. The distillation therefore separates **what is directly observable** from what would require fabricated precision.

Observed for all 30 papers:
- title, authorship, venue/version, abstract or equivalent paper summary;
- research-question framing;
- design/data/result verbs;
- order of design, result, mechanism, and scope claims in the abstract.

Observed for a broad cross-author subset:
- introduction openings and first-page paragraph progression;
- longer identification/design exposition;
- result/magnitude narration;
- mechanism qualification;
- conclusion/scope passages where public full text or author manuscripts were accessible.

Representative full-text or long-form inspection includes papers from every focal-author stratum. PDF/HTML availability differs by publisher, so this v1 bundle does **not** report fabricated corpus-wide sentence-length means, passive-voice percentages, or punctuation frequencies.

## Distillation gate

A candidate pattern was retained only when it met all of the following:

1. **Cross-author support:** observed in at least 4 of 6 focal-author strata.
2. **Task comparability:** compared within similar rhetorical jobs (e.g., result sentence with result sentence), not by pooled word frequency.
3. **Topic suppression:** discipline-specific nouns, named institutions, technologies, countries, and variables do not count as voice.
4. **Scientific-style non-duplication:** rules already governed by the scientific Style Bundle are not redefined here. Elite Voice controls realization, not evidentiary permission.
5. **Coauthor caution:** no single coauthored paper can establish a focal author's private voice.
6. **Leave-one-author robustness:** VOICE_SIGNATURE rules are designed to remain defensible if any one source-author stratum is removed.

## Main ensemble findings

### 1. Research actions are stated with explicit agents and specific verbs

Across the corpus, first-person plural is functional rather than conversational: *we study, use, construct, exploit, estimate, find, document, show*. Passive constructions are not forbidden, but active research-agent syntax is preferred when it clarifies who did what.

### 2. High-level prose is concrete rather than ornamental

Sentences tend to carry an identifiable object: a dataset, treatment, contrast, parameter, estimate, institution, or observable implication. Rhetorical force comes from the object and its evidence, not from evaluative adjectives.

### 3. Quantities are integrated into claims

When a number matters, it normally appears inside the substantive sentence and is translated against a baseline, control group, counterfactual, share, or other interpretable comparator. Regression apparatus is not used as a substitute for meaning.

### 4. Contrast is a major syntactic engine

The corpus repeatedly advances arguments through explicit matched contrasts: before/after, treated/control, high/low, one explanation/another, descriptive/causal, short-run/long-run. Simple connectors such as *but, while, whereas, in contrast,* and *however* do more work than decorative transition phrases.

### 5. Hedging is local

Facts, sample construction, treatment assignment, and reported estimates are generally stated directly. Hedging concentrates on mechanism attribution, external validity, rival explanations, and interpretation. This aligns with the existing Scientific Style Bundle and never weakens its claim-evidence rules.

### 6. Sentence complexity serves research logic

The source authors vary substantially in sentence length. The commonality is not a fixed length target but linear logical order: premise or variation → research action → readout → implication. Long sentences are accepted when each clause has a clear causal/comparative relation; short sentences are used to land a fact or contrast.

### 7. Enumeration is structural, not decorative

Numbered or "First/Second/Third" exposition is common when a paper genuinely has multiple independent facts or tests, especially in Chetty/Qian/Wang/Yang-style empirical exposition. It is not treated as a universal signature and should never be manufactured to create a rule-of-three effect.

### 8. Literature positioning is consequence-driven

Strong passages do not merely list papers. They state what earlier work can establish, what remains unresolved, and what the present design changes about the evidentiary frontier.

## Source-stratum tendencies (non-authoritative)

These notes explain where some ensemble traits are especially visible. They are **not** templates to imitate literally.

- **Acemoglu stratum:** argumentative framing, explicit confrontation of identification threats and rival views, dense but logically ordered sentences, careful mechanism caveats.
- **Chetty stratum:** unusually clear enumeration of empirical facts, natural magnitude translation, direct comparison to baselines, sharp descriptive/causal boundary.
- **Fang stratum:** efficient theory/prediction/evidence bridges, compact institution-to-mechanism exposition, direct quantitative contrasts.
- **Qian stratum:** puzzle/reversal framing, historical fact → identification movement, explicit multi-step empirical logic.
- **Wang stratum:** institution → design → quantified estimate → mechanism sequence, concise applied-micro result prose, clear policy/institutional objects.
- **Yang stratum:** question/contrast-driven political-economy framing, experiment/design stated early, explicit scope caveats and theoretical implications.

## What was intentionally not distilled

- topic nouns or preferred research subjects;
- memorable phrases or sentence-level mimicry;
- author-specific metaphors;
- fixed sentence-length targets;
- journal formatting;
- evidentiary rules already present in `style-bundle/`;
- claims about individual authorship that cannot be separated from coauthors.

## Validation status

This is **v1.0.0**. It passes:
- balanced-corpus gate;
- no duplicate paper gate;
- six-author coverage;
- scientific-style precedence check;
- no verbatim-example policy.

A future v1.1 could add a fully local full-text parse of all 30 source PDFs/HTML files and compute section × rhetorical-move sentence metrics. Until then, this bundle intentionally avoids pseudo-precise numerical style statistics.
