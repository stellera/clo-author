# Elite Economics Voice Bundle

This bundle is a corpus-derived prose layer for empirical economics.

It is built from a balanced 30-paper corpus associated with:
- Daron Acemoglu
- Raj Chetty
- Hanming Fang
- Nancy Qian
- Shaoda Wang
- David Y. Yang

The bundle is **not** an author-impersonation system. It transfers ensemble writing mechanisms that recur across the corpus while suppressing signature wording, topic vocabulary, and identifiable phrases.

## Required runtime files

- `VOICE_SPEC.md` — authoritative rule set
- `VOICE_MANIFEST.md` — section/move router
- `MOVE_REALIZATION.md`
- `HEDGING_AND_CLAIM_VOICE.md`
- `SENTENCE_RHYTHM.md`
- `PARAGRAPH_RHYTHM.md`
- `TRANSITIONS.md`
- `CITATION_VOICE.md`
- `VOICE_CRITIC_CHECKS.md`

Optional:
- `VOICE_EXAMPLES.md` — synthetic examples only
- `SOURCE_PROFILES.md` — provenance notes, never an imitation prompt
- `CORPUS_MANIFEST.md` — locked 30-paper corpus
- `DISTILLATION_REPORT.md` — methodology and limitations

## Rule classes

- `EV-SIG-*`: ensemble signatures; material drift can be flagged.
- `EV-DEF-*`: strong prose defaults; advisory unless clarity suffers.
- `EV-OPT-*`: legitimate alternatives; never penalize non-use.
- `EV-AVOID-*`: negative voice patterns; repeated/conspicuous violations can be flagged.
- `EVC-*`: operational critic checks.

## What this layer controls

- active versus obscuring passive syntax;
- research/reporting verb choice;
- magnitude integration;
- comparator use;
- matched contrastive syntax;
- local hedging;
- clause order;
- result paragraph openings;
- transitions;
- citation voice;
- paragraph closure and rhythm.

## What this layer does not control

- whether a claim is causal;
- whether a mechanism is identified;
- which empirical design is valid;
- which result is substantively true;
- section-level evidence architecture already governed by the Scientific Style Bundle;
- journal format;
- topic vocabulary.

Those higher-order constraints come from actual evidence, content invariants, and `.claude/references/style-bundle/`.

## Loading order

1. Scientific Style determines what the evidence permits.
2. Elite Voice chooses a high-quality linguistic realization inside that permitted space.
3. Personal voice, if present, is a lower-priority optional overlay.

## Update policy

To refresh the corpus-derived voice:
- keep the author-balanced corpus design;
- do not overweight prolific authors;
- de-duplicate shared papers;
- require cross-author support for EV-SIG rules;
- avoid pseudo-precise sentence metrics unless every source text is locally parsed and reproducibly measured;
- keep all examples synthetic.
