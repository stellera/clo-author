# Assertiveness and Anti-Defensiveness Policy

**Role:** operational overlay for the corpus-derived Scientific Writing Style Bundle.

This file does **not** change what the evidence permits. `STYLE_SPEC.md` and `CLAIM_EVIDENCE_RULES.md` remain authoritative for claim strength. This policy controls how often, where, and how qualifications are expressed so that correct epistemic calibration does not turn into defensive prose.

## Core principle

> State the strongest claim the warrant actually licenses, state it directly, and qualify only the dimension that is genuinely limited.

A well-calibrated sentence is not a timid sentence. A design-identified effect should be written as an effect. A descriptive association should be written directly as an association. A suggestive mechanism should receive one calibrated attribution, not a stack of apologies.

## ASSERT-01 — Claim first, qualification second

When the evidence licenses a substantive claim, lead with that claim or its quantitative readout. Do not preface it with generic caution.

Prefer:
> The reform increased formal employment by 4.2 percentage points. The estimate applies to firms observed around the eligibility threshold.

Avoid:
> While the estimates should be interpreted with caution and may not generalize broadly, the reform appears to have increased formal employment.

A qualifier may share the sentence when it is short and essential to the estimand, but it should not delay the main verb.

## ASSERT-02 — One material boundary, one full statement

State a material limitation fully at the first inferential point where it matters. Do not restate the same caveat in every later section.

After the boundary has been established:
- use the correctly scoped noun phrase ("among incumbent firms", "over the two-year window");
- or omit repetition when the scope is already salient.

Do not repeat the same external-validity or identification disclaimer in the introduction, results, robustness, and conclusion unless the later context would otherwise materially mislead the reader.

## ASSERT-03 — Qualify the dimension, not the whole finding

A limitation should attach to the specific dimension that is limited:

- **population:** "among firms near the cutoff";
- **time:** "over the first two post-reform years";
- **mechanism:** "consistent with supplier substitution";
- **precision:** "the interval excludes effects larger than 2 percent";
- **external validity:** "the design speaks directly to urban counties."

Avoid global softeners such as:
- "these results should be interpreted with caution";
- "we cannot draw strong conclusions";
- "the evidence is only suggestive" when only the mechanism attribution is suggestive.

## ASSERT-04 — Prefer evidence-based uncertainty to lexical uncertainty

When possible, express uncertainty with the object that creates it:

- confidence interval;
- standard error;
- pre-trend estimate;
- placebo result;
- first stage;
- balance check;
- sample coverage;
- identified population.

Prefer:
> The estimate is 3.1 percentage points (95% CI: 1.2 to 5.0).

over:
> The treatment may have had a positive effect.

Prefer:
> Pre-treatment coefficients are small and jointly insignificant.

over:
> Although the parallel-trends assumption cannot be proven, it appears plausible.

## ASSERT-05 — Do not stack hedges

Use at most one epistemic hedge for a single inferential step unless two distinct uncertainties are being expressed.

Avoid:
> The pattern may perhaps be consistent with the possibility that...

Prefer:
> The pattern is consistent with...

Avoid:
> We cannot rule out that the effect may partly reflect...

Prefer, when accurate:
> The design does not distinguish this channel from X.

## ASSERT-06 — Robustness checks may share a scope verdict

`HARD-ROBUST-01` should be implemented at the level of a **logical check unit**, not mechanically once per paragraph or specification.

A cluster of checks addressing the same threat may use:
1. one sentence/paragraph naming the perturbations;
2. compact readouts;
3. one scope verdict for the cluster.

Do not append a defensive sentence after every robustness estimate.

Prefer:
> The estimate is stable when we add region trends, drop the largest cities, and reweight by baseline population. Together, these checks make differential regional trends an unlikely explanation for the baseline result.

Avoid three separate paragraphs each ending with a variant of:
> Nevertheless, this check cannot rule out all remaining confounding.

## ASSERT-07 — Robustness closes named threats; it does not rehearse universal uncertainty

After a check addresses the threat it was designed to test, state the bounded conclusion directly.

Allowed:
> This makes selective attrition an unlikely explanation for the estimate.

Do not add universal disclaimers such as:
- "of course, no robustness test can establish causality";
- "other unobserved factors may remain";
- "these checks do not rule out every possible concern";

unless a **specific, material unresolved threat** is known and relevant.

## ASSERT-08 — Mechanism calibration should be precise, not apologetic

For suggestive mechanism evidence:
1. report the channel evidence directly;
2. use one calibrated attribution phrase;
3. move on.

Prefer:
> Effects are larger where alternative suppliers were scarce. This gradient is consistent with substitution capacity mediating adjustment.

Avoid:
> Although this evidence is only suggestive and cannot definitively establish the mechanism, it may nevertheless be broadly consistent with the possibility that substitution capacity could matter.

Once a paragraph has stated "consistent with" or equivalent, subsequent sentences may discuss the observed gradient directly without repeating the hedge.

## ASSERT-09 — Data restrictions are prioritized by inferential consequence

`HARD-DATA-01` requires timely disclosure of restrictions that change:
- the estimand;
- sample representativeness;
- measurement validity;
- treatment/control construction;
- interpretation of the main outcome.

Routine cleaning rules, coding details, minor missingness conventions, and technical exclusions that do not change the reader's interpretation may be grouped, footnoted, or moved to an appendix.

Do not turn the data section into a chronological list of every possible imperfection.

## ASSERT-10 — Conclusions lead with the answer, not the caveat

The conclusion should first state:
- the answer;
- the central magnitude or substantive meaning;
- the contribution/implication at the licensed strength.

A limitation paragraph is **not mandatory**.

Include a scope/limitation statement only when it materially changes how the result should be interpreted or used. If the limitation has already been established in the body, a concise scoped formulation is sufficient.

Prefer:
> The reform increased formal employment among firms near the threshold, with an effect equal to 18 percent of the baseline mean. The result shows that enforcement capacity can materially change policy incidence.

Then, if needed:
> The design identifies responses near the threshold; effects for much larger firms remain outside the estimand.

Avoid ending the paper with a catalogue of generic limitations or future-work disclaimers.

## ASSERT-11 — Generalization is bounded positively

When external validity is limited, state what the evidence **does** cover before what it does not.

Prefer:
> The evidence speaks directly to incumbent urban manufacturers and is most likely to extend to settings with similar enforcement technology.

Avoid:
> These results may not generalize to other populations, periods, countries, industries, or institutional settings.

## ASSERT-12 — Do not underclaim identified results

The Critic should treat systematic underclaiming as a style defect when the design clearly licenses a stronger statement.

Examples:
- causal design + passed identifying checks → "is associated with" may be unnecessarily weak;
- documented fact → "appears to be" is unnecessarily weak;
- precise estimate → "may have increased" is unnecessarily weak.

This rule never authorizes stronger language than `CLAIM_EVIDENCE_RULES.md`. It requires using the strongest **already-licensed** band rather than defaulting to a weaker one.

## Defensive-writing anti-patterns

### DW-01 — Caveat-first sentence
The sentence opens with "although/while/despite a limitation..." and delays a well-supported main result without a substantive reason.

### DW-02 — Repeated caveat
The same identification, scope, or external-validity caveat is fully restated in multiple sections.

### DW-03 — Hedge stack
Two or more lexical hedges are used for a single inferential uncertainty.

### DW-04 — Universal disclaimer
A paragraph adds "cannot rule out all concerns / other factors may remain" without naming a specific unresolved threat.

### DW-05 — Defensive robustness tail
Each robustness check ends with a generic disclaimer instead of a bounded verdict.

### DW-06 — Limitation catalogue
The conclusion or discussion lists generic limitations that do not materially change interpretation.

### DW-07 — Underclaiming below the warrant
The prose uses a weaker evidentiary band than the named design/checks license.

### DW-08 — Qualification duplication
A scope condition already encoded in the estimand/population noun phrase is restated as a separate apologetic sentence.

## Section defaults

### Introduction
- Preview the result directly at its licensed strength.
- One scope qualifier is enough.
- Do not front-load limitations before the reader knows the finding.

### Data
- Disclose material restrictions early.
- Group minor implementation details.
- Do not apologize for ordinary measurement choices; explain and validate them.

### Empirical Strategy
- State assumptions directly.
- Defend them with implications and checks, not with lexical modesty.
- Do not write "we cannot prove the assumption"; state what observable evidence supports it.

### Results
- Result → number → interpretation.
- No caveat between the result and its magnitude unless the qualifier is part of the estimand itself.
- Do not append a limitation to every result paragraph.

### Mechanism
- One calibrated attribution per inferential step.
- Direct channel readout stays direct; uncertainty attaches to attribution.

### Robustness
- Group checks by threat.
- One scope verdict can close multiple related checks.
- Do not rehearse universal uncertainty.

### Conclusion
- Answer first.
- Scope only if material.
- No mandatory limitation paragraph.
- Do not end on an apology.

## Critic interpretation

A draft is **not** better merely because it contains more caveats.

The critic should ask:
1. Is the claim stronger than the warrant? If yes, flag overclaim.
2. Is the claim weaker than the warrant without a substantive reason? If yes, flag underclaim.
3. Is the same qualification repeated? If yes, compress it.
4. Is the uncertainty expressed by evidence/precision where possible? If no, replace generic hedging.
5. Does a caveat materially change interpretation? If no, remove it.

The target is calibrated confidence: neither overclaiming nor defensive underclaiming.
