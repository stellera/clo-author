# Elite Economics Voice Manifest

**Authoritative source:** `VOICE_SPEC.md`

This file routes the Elite Voice Bundle into Clo-Author without loading every voice asset on every call.

## Always load

- `EV-SIG-01` through `EV-SIG-06`
- `EV-AVOID-01` through `EV-AVOID-06`
- relevant entries in `HEDGING_AND_CLAIM_VOICE.md`
- `MOVE_REALIZATION.md` entries for the rhetorical moves used in the target section

Scientific Style Bundle rules always have higher priority.

## abstract

Load:
- EV-SIG-01, 03, 04, 05, 06, 09
- EV-DEF-03, 04
- EV-OPT-03
- MOVE_REALIZATION: RESEARCH_QUESTION, DATA/DESIGN, MAIN_RESULT, MAGNITUDE, GENERALIZATION
- Voice checks EVC-01, 03, 04, 06, 12

## introduction

Load:
- EV-SIG-01 through 10
- EV-DEF-01 through 07, 10
- EV-OPT-01, 02, 03, 04, 05
- TRANSITIONS.md
- CITATION_VOICE.md
- MOVE_REALIZATION: PHENOMENON, PUZZLE, UNKNOWN, RESEARCH_QUESTION, SETTING, DATA, IDENTIFICATION, MAIN_RESULT, MAGNITUDE, CONTRIBUTION, LITERATURE_POSITION

## literature

Load:
- EV-SIG-02, 03, 05, 08, 10
- EV-DEF-05, 06, 07
- CITATION_VOICE.md
- MOVE_REALIZATION: LITERATURE_POSITION, CONTRIBUTION

## institutional_background

Load:
- EV-SIG-02, 03, 05, 08
- EV-DEF-05, 07, 10
- MOVE_REALIZATION: SETTING, MEASUREMENT, IDENTIFICATION
- TRANSITIONS.md

## data

Load:
- EV-SIG-01, 02, 03, 07, 08
- EV-DEF-01, 05, 07, 10
- MOVE_REALIZATION: DATA, MEASUREMENT, VALIDATION
- SENTENCE_RHYTHM.md

## empirical_strategy

Load:
- EV-SIG-01, 02, 03, 05, 07, 08
- EV-DEF-01, 05, 07, 10
- MOVE_REALIZATION: SPECIFICATION, IDENTIFICATION, IDENTIFYING_ASSUMPTION, IDENTIFICATION_THREAT, VALIDATION
- SENTENCE_RHYTHM.md
- TRANSITIONS.md

## results

Load:
- EV-SIG-01 through 10
- EV-DEF-01, 03, 05, 07, 08, 09, 10
- MOVE_REALIZATION: MAIN_RESULT, MAGNITUDE, HETEROGENEITY, NULL_RESULT, ROBUSTNESS
- SENTENCE_RHYTHM.md
- PARAGRAPH_RHYTHM.md
- HEDGING_AND_CLAIM_VOICE.md

## mechanism

Load:
- EV-SIG-01, 02, 03, 05, 06, 07, 08, 10
- EV-DEF-03, 05, 07, 10
- MOVE_REALIZATION: MECHANISM, HETEROGENEITY, ALTERNATIVE_EXPLANATION, NULL_RESULT
- HEDGING_AND_CLAIM_VOICE.md
- TRANSITIONS.md

## robustness

Load:
- EV-SIG-01, 02, 03, 05, 06, 08, 10
- EV-DEF-03, 05, 07, 10
- MOVE_REALIZATION: ROBUSTNESS, IDENTIFICATION_THREAT, NULL_RESULT
- HEDGING_AND_CLAIM_VOICE.md

## conclusion

Load:
- EV-SIG-02, 03, 04, 05, 06, 09, 10
- EV-DEF-05, 07, 08, 10
- EV-OPT-02, 04, 05
- MOVE_REALIZATION: CONTRIBUTION, MAIN_RESULT, MAGNITUDE, LIMITATION, GENERALIZATION
- PARAGRAPH_RHYTHM.md

## Optional resources

- `VOICE_EXAMPLES.md`: synthetic examples only; load only when drafting needs a concrete realization.
- `SOURCE_PROFILES.md`: provenance/context only; never use as an imitation prompt.
- `CORPUS_MANIFEST.md` and `DISTILLATION_REPORT.md`: audit trail, not drafting context.

## Rule levels

- **EV-SIG-***: ensemble signature; critic can flag material drift.
- **EV-DEF-***: strong default; deviation requires no penalty unless it harms clarity or coherence.
- **EV-OPT-***: legitimate option; never penalize non-use.
- **EV-AVOID-***: negative voice rule; flag repeated or conspicuous violations.

## Context discipline

Do not load the entire bundle into context. Read this manifest, then retrieve only the rules/files needed for the target section and rhetorical moves.
