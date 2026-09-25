# Distilled Writing Style Bundle

This directory is the stable integration point between an external style-distillation pipeline and clo-author.

## Drop-in contract

After distillation, place the generated files here without renaming them:

- `STYLE_SPEC.json` — authoritative machine-readable style policy
- `STYLE_SPEC.md` — human-readable projection of the policy
- `SECTION_GRAMMARS.md` — section-specific rhetorical sequences and paragraph architectures
- `CLAIM_EVIDENCE_RULES.md` — evidence-to-claim calibration and epistemic-strength rules
- `FORBIDDEN_PATTERNS.md` — corpus-grounded anti-patterns and prohibited constructions
- `STYLE_EXAMPLES.md` — synthetic/abstracted examples indexed by section or rhetorical move
- `STYLE_CRITIC_CHECKS.md` — critic-facing checks derived from the style policy

Only `STYLE_SPEC.json` is authoritative. If a Markdown projection conflicts with it, follow `STYLE_SPEC.json`.

## Activation

The bundle is **active** when `writing_style/STYLE_SPEC.json` exists and is non-empty.

When active:

1. Writer and review workflows must load the bundle automatically.
2. Claim-evidence calibration applies before personal voice preferences.
3. Section grammar is loaded for the section currently being drafted or reviewed.
4. `HARD_RULE` items are binding unless they conflict with empirical truth, content invariants, identification requirements, or working-paper-format rules.
5. `STRONG_DEFAULT` items are defaults, not mechanical templates; systematic departures should be diagnosed, not blindly rewritten.
6. `OPTIONAL_STYLE` items may be overridden by a populated personal style guide.
7. `ANTI_PATTERN` and forbidden-pattern rules apply during cleanup and review.
8. Examples are retrieval aids only; never copy corpus language verbatim into a manuscript.

## Priority order

When instructions conflict, use this precedence:

1. Actual data, estimates, tables, figures, and verified citations
2. Content invariants and identification fidelity
3. Working-paper-format requirements
4. Distilled claim-evidence rules and `HARD_RULE` items
5. Distilled section grammars and `STRONG_DEFAULT` items
6. Populated `.claude/references/personal-style-guide.md`
7. Distilled `OPTIONAL_STYLE` items
8. Generic clo-author templates/default academic prose

A personal voice preference can never strengthen a claim beyond what the evidence permits.

## Relationship to personal-style-guide.md

The two systems serve different purposes:

- `writing_style/` = scientific writing policy distilled from a target corpus
- `.claude/references/personal-style-guide.md` = the user's personal voice

A valid distilled bundle is sufficient for drafting. A personal style guide is optional when the bundle is active and, when present, is layered on top only where it does not conflict with higher-priority rules.

## Upgrade safety

This directory lives outside `.claude/` intentionally. Clo-author's `/tools upgrade` replaces `.claude/` but does not touch `writing_style/` or root `CLAUDE.md`.

After any infrastructure upgrade, the integration contract in root `CLAUDE.md` remains authoritative.
