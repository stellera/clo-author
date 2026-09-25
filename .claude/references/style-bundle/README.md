# Distilled Style Bundle

This directory contains the corpus-distilled scientific writing policy used directly by Clo-Author's Writer and Writer-Critic.

## Active bundle

The current bundle is version 1.0.0 and is Markdown-native.

Required files:

- `STYLE_SPEC.md` — **authoritative specification**
- `STYLE_MANIFEST.md` — Clo-Author routing layer for section-specific rule loading
- `SECTION_GRAMMARS.md` — section-level rhetorical sequences
- `CLAIM_EVIDENCE_RULES.md` — evidence-to-claim licensing and epistemic calibration
- `FORBIDDEN_PATTERNS.md` — corpus-supported anti-patterns / critic defaults
- `STYLE_CRITIC_CHECKS.md` — executable critic questions

Optional:

- `STYLE_EXAMPLES.md` — synthetic examples used only as examples, never as scoring authority

The bundle is active only when every required file exists.

If companion files conflict with `STYLE_SPEC.md`, follow `STYLE_SPEC.md`.

## How Writer uses the bundle

Writer reads `STYLE_MANIFEST.md` first, then loads:

1. cross-cutting claim/evidence rules;
2. only the target section's rules from `STYLE_SPEC.md`;
3. the matching section grammar;
4. relevant anti-patterns and critic checks;
5. examples only when useful.

This avoids filling the context window with unrelated style material.

Key corpus policies include:

- introductions frame first, state the gap/question by paragraph 3, then preview quantified findings;
- results report numerical evidence before interpretation and translate headline magnitudes;
- empirical strategy contains identification objects/assumptions/checks, not estimated readouts;
- heterogeneity and gradients remain suggestive unless a direct channel-specific test is present;
- robustness follows perturbation → readout → scope verdict;
- data provenance/restrictions are disclosed before the object carries evidentiary weight;
- conclusions separate verdict from scope and do not introduce new estimands.

## How Writer-Critic uses the bundle

Writer-Critic uses:

- `CLAIM_EVIDENCE_RULES.md` in Claims and Evidence;
- `FORBIDDEN_PATTERNS.md` in Writing Quality;
- `STYLE_SPEC.md`, `STYLE_MANIFEST.md`, `SECTION_GRAMMARS.md`, and `STYLE_CRITIC_CHECKS.md` in Style Fidelity.

Every distilled-style finding should cite a rule/check ID such as:

- `HARD-RESULT-01`
- `HARD-MECH-01`
- `AP-CLAIM-01`
- `CHK-04`

## Rule levels

- `HARD-*`: binding unless a higher-priority empirical/content invariant requires departure.
- `DEF-*`: strong default; deviation needs a substantive reason.
- `OPT-*`: optional style; never penalize non-use.
- `AP-*`: anti-pattern / critic default.
- `CHK-*`: operational diagnostic check.

## Claim-evidence priority

The bundle never upgrades an empirical claim. Priority is:

1. actual data, code output, tables, figures, and verified citations;
2. content invariants and identification fidelity;
3. `CLAIM_EVIDENCE_RULES.md`;
4. `HARD-*` rules in `STYLE_SPEC.md`;
5. working-paper-format rules;
6. section grammars and `DEF-*` defaults;
7. personal voice;
8. generic Clo-Author templates;
9. `OPT-*` preferences and examples.

Personal voice may choose among permitted stylistic variants, but it cannot override evidentiary calibration.

## Distillation output contract

A style-distillation workflow can refresh this bundle by replacing the six distillation outputs:

```text
.claude/references/style-bundle/
├── STYLE_SPEC.md
├── SECTION_GRAMMARS.md
├── CLAIM_EVIDENCE_RULES.md
├── FORBIDDEN_PATTERNS.md
├── STYLE_CRITIC_CHECKS.md
└── STYLE_EXAMPLES.md
```

`STYLE_MANIFEST.md` is the Clo-Author integration layer. Update it only when rule IDs, section names, or bundle structure change materially.
