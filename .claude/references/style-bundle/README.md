# Distilled Style Bundle

This directory is the drop-in interface between a style-distillation pipeline and Clo-Author's existing writing/review workflow.

The distillation process should write its final artifacts **directly into this directory**. Clo-Author does not generate these files during normal `/write` operations.

## Required files

A bundle is considered active only when all of the following exist:

| File | Role |
|---|---|
| `STYLE_SPEC.json` | **Authoritative source of truth** for distilled rules, levels, applicability, support, and rule IDs |
| `SECTION_GRAMMARS.md` | Human/agent-readable rhetorical grammars by section |
| `CLAIM_EVIDENCE_RULES.md` | Evidence-to-claim calibration and epistemic-language constraints |
| `FORBIDDEN_PATTERNS.md` | Corpus-supported anti-patterns / prohibited writing patterns |
| `STYLE_CRITIC_CHECKS.md` | Operational checks for the writer-critic |

Optional:

| File | Role |
|---|---|
| `STYLE_EXAMPLES.md` | Synthetic or short corpus-grounded examples used only as a retrieval/example bank |

If `STYLE_SPEC.json` exists but one or more required companion files are missing, Writer treats the bundle as invalid and stops rather than silently combining inconsistent assets.

## Integration behavior

### Writer

When the bundle is active, Writer automatically loads:

1. global HARD_RULES from `STYLE_SPEC.json`;
2. rules applicable to the requested section;
3. `CLAIM_EVIDENCE_RULES.md`;
4. the target section's material from `SECTION_GRAMMARS.md`;
5. `FORBIDDEN_PATTERNS.md`;
6. `STYLE_EXAMPLES.md` only when examples are genuinely useful.

The bundle governs argument organization, rhetorical sequence, claim strength, epistemic calibration, and documented anti-patterns.

### Writer-Critic

When the bundle is active:

- Category 2 checks `CLAIM_EVIDENCE_RULES.md`;
- Category 4 checks `FORBIDDEN_PATTERNS.md`;
- Category 7A checks `STYLE_SPEC.json`, `SECTION_GRAMMARS.md`, and `STYLE_CRITIC_CHECKS.md`.

Every style-specific deduction should cite the corresponding rule ID.

## Relationship to personal-style-guide.md

The two systems have different jobs:

- **Distilled Style Bundle:** scientific/rhetorical writing policy learned from the target paper corpus.
- **personal-style-guide.md:** the user's personal voice, punctuation, lexicon, and sentence-level habits.

A valid Distilled Style Bundle is sufficient to unblock drafting even if the personal style guide is still a template.

When both are active, the bundle has higher priority for claim-evidence discipline, HARD_RULES, and section grammar. Personal voice operates only within the allowed space.

## Precedence

When instructions conflict:

1. actual data, code output, tables, figures, and verified citations;
2. content invariants and identification fidelity;
3. `CLAIM_EVIDENCE_RULES.md`;
4. HARD_RULES in `STYLE_SPEC.json`;
5. working-paper-format rules;
6. section grammar and STRONG_DEFAULTS;
7. personal style guide;
8. generic Clo-Author templates;
9. OPTIONAL_STYLE preferences and examples.

No style rule may strengthen a claim beyond what the evidence supports.

## Section names

The distillation pipeline should use stable section labels where possible:

- `abstract`
- `introduction`
- `literature`
- `background`
- `data`
- `empirical_strategy`
- `model`
- `results`
- `mechanism`
- `heterogeneity`
- `robustness`
- `discussion`
- `conclusion`

Clo-Author command aliases map as follows:

- `/write intro` -> `introduction`
- `/write strategy` -> `empirical_strategy` (or model/estimation for the detected paper type)
- `/write results` -> `results`, with mechanism/heterogeneity/robustness rules loaded only when relevant
- `/write conclusion` -> `conclusion`
- `/write abstract` -> `abstract`

## STYLE_SPEC.json expectations

The exact schema may evolve, but each rule should expose enough information for deterministic use:

```json
{
  "rule_id": "RESULT-004",
  "level": "HARD_RULE",
  "applicable_sections": ["results"],
  "applicable_moves": ["MAIN_RESULT", "MAGNITUDE"],
  "rule_statement": "State quantitative evidence before substantive interpretation.",
  "support": {
    "paper_count": 23,
    "paper_share": 0.77,
    "paragraph_count": 81
  }
}
```

Recommended rule levels:

- `HARD_RULE`
- `STRONG_DEFAULT`
- `OPTIONAL_STYLE`
- `ANTI_PATTERN`

The Writer and Writer-Critic must not turn `OPTIONAL_STYLE` into a requirement.

## Recommended distillation output command

Configure the external/Codex style-distillation workflow so its final rendering step writes:

```text
.claude/references/style-bundle/
├── STYLE_SPEC.json
├── SECTION_GRAMMARS.md
├── CLAIM_EVIDENCE_RULES.md
├── FORBIDDEN_PATTERNS.md
├── STYLE_EXAMPLES.md
└── STYLE_CRITIC_CHECKS.md
```

No manual copying or conversion should be necessary after distillation.
