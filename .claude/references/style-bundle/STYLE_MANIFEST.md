# Style Bundle Manifest

This manifest integrates the distilled Scientific Writing Style Specification v1.0.0 into Clo-Author.

## Authority

`STYLE_SPEC.md` is the authoritative specification for this bundle. Companion files operationalize it:

- `CLAIM_EVIDENCE_RULES.md` — evidence-to-claim licensing
- `SECTION_GRAMMARS.md` — section-level rhetorical sequences
- `FORBIDDEN_PATTERNS.md` — critic defaults and anti-patterns
- `STYLE_CRITIC_CHECKS.md` — executable review questions
- `STYLE_EXAMPLES.md` — synthetic examples only; never a scoring authority

If companion wording conflicts with `STYLE_SPEC.md`, follow `STYLE_SPEC.md`.

## Cross-cutting rules

Always load these regardless of section:

- `HARD-CLAIM-01` — claim strength follows the named warrant
- `HARD-LEX-01` — argumentative force comes from evidence/checks, not intensifying verbs
- `AP-CLAIM-01` — heterogeneity/mediator evidence cannot inherit causal mechanism strength
- `AP-CLAIM-02` — hedging belongs on interpretation/reach, not uniformly across factual and evidentiary sentences
- `CLAIM_EVIDENCE_RULES.md` in full

## Section rule map

### abstract
Load:
- `HARD-INTRO-04`
- `HARD-CLAIM-01`
- `HARD-MECH-01`
- `HARD-DATA-02`
- `DEF-ABSTRACT-01`, `DEF-ABSTRACT-02`
- `AP-CLAIM-01`, `AP-CONCL-02`, `AP-GEN-01`
- abstract grammar and `CHK-17`

### introduction
Load:
- `HARD-INTRO-01` through `HARD-INTRO-04`
- `HARD-CLAIM-01`
- `HARD-RESULT-03`
- `DEF-INTRO-01` through `DEF-INTRO-05`
- `AP-INTRO-01` through `AP-INTRO-03`
- `AP-CLAIM-02`, `AP-CONCL-02`
- introduction grammars and `CHK-01`, `CHK-02`

### literature
Load:
- `DEF-INTRO-04`
- `DEF-LIT-01`, `DEF-LIT-02`
- `AP-LIT-01`
- literature grammar

### institutional_background
Load:
- `HARD-DATA-02`
- `HARD-BKGD-01`
- `AP-CLAIM-02`, `AP-DATA-01`
- institutional-background grammar

### data
Load:
- `HARD-STRATEGY-02`
- `HARD-DATA-01`, `HARD-DATA-02`
- `HARD-LEX-01`
- `DEF-DATA-01`
- `AP-CLAIM-02`, `AP-DATA-01`, `AP-DATA-02`
- data grammar and `CHK-12`, `CHK-13`

### empirical_strategy
Load:
- `HARD-STRATEGY-01`, `HARD-STRATEGY-02`
- `HARD-LEX-01`
- `AP-CLAIM-02`, `AP-STRATEGY-01`, `AP-STRATEGY-02`
- empirical-strategy grammars and `CHK-07`, `CHK-08`, `CHK-09`

### results
Load:
- `HARD-CLAIM-01`
- `HARD-RESULT-01` through `HARD-RESULT-03`
- `HARD-MECH-01`
- `HARD-DATA-02`
- `HARD-LEX-01`
- `DEF-RESULT-01` through `DEF-RESULT-03`
- `AP-CLAIM-01`, `AP-RESULT-01` through `AP-RESULT-03`
- results grammars and `CHK-03` through `CHK-06`, `CHK-16`

### mechanism
Load:
- `HARD-CLAIM-01`
- `HARD-STRATEGY-02`
- `HARD-MECH-01`, `HARD-MECH-02`
- `HARD-LEX-01`
- `DEF-MECH-01`
- `AP-CLAIM-01`, `AP-CLAIM-02`, `AP-RESULT-01`
- mechanism grammars and `CHK-03`, `CHK-04`, `CHK-09`, `CHK-16`

### robustness
Load:
- `HARD-CLAIM-01`
- `HARD-STRATEGY-02`
- `HARD-ROBUST-01`, `HARD-ROBUST-02`
- `HARD-MECH-01`
- `HARD-DATA-02`
- `HARD-LEX-01`
- `AP-CLAIM-01`, `AP-RESULT-01`, `AP-ROBUST-01`, `AP-ROBUST-02`
- robustness grammars and `CHK-10`, `CHK-11`, `CHK-16`

### conclusion
Load:
- `HARD-CLAIM-01`
- `HARD-RESULT-03`
- `HARD-MECH-01`
- `HARD-DATA-02`
- `HARD-CONCL-01`, `HARD-CONCL-02`
- `DEF-CONCL-01`, `DEF-CONCL-02`
- `AP-CLAIM-01`, `AP-CONCL-01`, `AP-CONCL-02`, `AP-GEN-01`
- conclusion grammars and `CHK-14`, `CHK-15`

## Rule levels

- **HARD_RULE:** binding unless a higher-priority empirical/content invariant requires departure.
- **STRONG_DEFAULT / DEF-***: expected default; deviation is acceptable when the manuscript has a clear substantive reason.
- **OPTIONAL_STYLE / OPT-***: never scored as a violation.
- **ANTI_PATTERN / AP-***: critic defaults; flag when the described pattern is actually present.

## Loading discipline

Do not load the entire Style Bundle into every drafting call.

For a section:
1. read this manifest;
2. read the matching rules in `STYLE_SPEC.md`;
3. read the matching grammar in `SECTION_GRAMMARS.md`;
4. read `CLAIM_EVIDENCE_RULES.md`;
5. read only relevant anti-patterns/checks;
6. use `STYLE_EXAMPLES.md` only if a concrete example would help.

This preserves context for the research content while keeping style enforcement explicit and traceable.
