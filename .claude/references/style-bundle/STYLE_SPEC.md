# Scientific Writing Style Specification


Version: `1.0.0`


## Hard Rules

### HARD-INTRO-01

Open the introduction on a framing slot only: the phenomenon, the stakes, the setting, the open question, or the state of knowledge as a foil. Slot 1 may not contain the estimator, the data inventory, the identification defence, or a result.

**Rationale.** Every profiled paper spends its first paragraph establishing what is being asked and why, before any machinery is named. The reader has to know which question a design answers before the design can be read as an answer.

**Support.** 15 papers · share 1.00 · corpus 1.00 · 15 paragraphs

_Evidence._ Introduction slot 1 is a framing move in all 12 profiles of distillation batch 1 and all 3 of batch 2; the opener-type disagreement between papers is which framing move (perception gap, dated policy episode, two-sided puzzle), not whether to frame.


**Applies to:** introduction


**Exceptions:** Papers whose first paragraph is the journal abstract merged into the introduction body (one AER-style paper) still open on prevalence and stakes rather than on design.

### HARD-INTRO-02

State the knowledge gap or the research question no later than the third introduction paragraph, and state it as something prior evidence cannot settle - not as a topic statement.

**Rationale.** The gap is what licenses everything after it in the introduction, including the right to preview results.

**Support.** 14/15 papers observable · share 0.93 · corpus 0.93 · 15 paragraphs

_Evidence._ 11 of 12 profiles in introduction batch 1 place UNKNOWN or RESEARCH_QUESTION by slot 3, and all 3 profiles in batch 2 place framing before the question.


**Applies to:** introduction

### HARD-INTRO-03

Preview at least one headline finding inside the introduction, and never before the gap has been stated. The preview is a digest - direction, headline magnitude, one scope qualifier - not a specification walk.

**Rationale.** Top-field introductions buy the reader's attention with the answer, but the answer is only informative once the question is on the table.

**Support.** 15 papers · share 1.00 · corpus 1.00 · 20 paragraphs

_Evidence._ MAIN_RESULT appears inside the introduction for all 12 profiles of batch 1 (first appearance never before slot 5) and all 3 profiles of batch 2.


**Applies to:** introduction


**Exceptions:** Theory-led papers preview a derived proposition rather than an estimate.

### HARD-INTRO-04

Give every previewed introduction finding at least one quantity - an estimate, a share, an elasticity, a prevalence, or a translated magnitude. Direction-only previews are not sufficient.

**Rationale.** The quantified preview is what distinguishes a claim about evidence from a statement of intent.

**Support.** 13/15 papers observable · share 0.87 · corpus 0.87 · 17 paragraphs

_Evidence._ 10 of 12 in introduction batch 1 plus all 3 in batch 2; the two exceptions are papers whose introduction carries no estimate at all.


**Applies to:** introduction, abstract

### HARD-CLAIM-01

Grade every claim by the warrant named in the same or an earlier paragraph - the design, instrument, cutpoint, randomization, check, model object, or measurement construction. Never let position in the document (abstract, introduction, conclusion) upgrade or downgrade the claim's strength.

**Rationale.** This is the single most consistent behaviour in the corpus and the one the style layer most needs to preserve: the same finding carries the same evidence label and the same hedging band wherever it is restated.

**Support.** 15 papers · share 1.00 · corpus 1.00 · 44 paragraphs

_Evidence._ Independent statements in introduction batch 1 (10/12), introduction batch 2 (3/3, as its own hard rule), conclusion batch 1 (9/9) and abstract (4/4).


**Applies to:** abstract, introduction, results, mechanism, robustness, conclusion

### HARD-RESULT-01

Never assert an effect in words alone: each MAIN_RESULT states at least one numeric quantity together with the object it measures, and the statistical apparatus (standard errors, column pointers, specification notation) stays attached to the estimate rather than to the interpretation.

**Rationale.** The results section's argumentative currency is the number; prose-only effect claims are read as unsupported.

**Support.** 10 papers · share 1.00 · corpus 0.67 · 250 paragraphs

_Evidence._ All 10 profiles with a results section; 48 of the corpus's MAIN_RESULT paragraphs carry a quantity.


**Applies to:** results

### HARD-RESULT-02

Report before you explain: no MECHANISM, HETEROGENEITY, ALTERNATIVE_EXPLANATION or LITERATURE_POSITION move may precede the section's first MAIN_RESULT paragraph.

**Rationale.** Interpretation arriving before the readout lets the reader believe the evidence is the interpretation.

**Support.** 8/10 papers observable · share 0.80 · corpus 0.53 · 96 paragraphs

_Evidence._ 8 of 10 results profiles; the two exceptions introduce a mechanism prediction first and then test it.


**Applies to:** results

### HARD-RESULT-03

Translate each headline estimate into a comparable unit (share of a base, per-standard-deviation, monetary, per-unit, rank) in the same paragraph or the next, before moving to a new object.

**Rationale.** A bare coefficient is not a finding a reader can weigh; every profiled paper anchors its headline to something outside the regression.

**Support.** 8/10 papers observable · share 0.80 · corpus 0.53 · 74 paragraphs

_Evidence._ 8 of 10 results profiles carry an explicit MAGNITUDE move adjacent to the estimate; corroborated by the results anti-pattern against bare-coefficient reporting (8/10).


**Applies to:** results, introduction, conclusion

### HARD-STRATEGY-01

State no findings in the empirical-strategy section: no MAIN_RESULT, no MAGNITUDE, no estimated quantity. Its deliverable is an object - an estimand, an assumption, a contrast, a checking plan.

**Rationale.** Once a number appears in the design argument, the reader starts weighing evidence that has not yet been shown to be identification.

**Support.** 8 papers · share 1.00 · corpus 0.53 · 75 paragraphs

_Evidence._ All 8 profiles with an empirical-strategy section; zero MAIN_RESULT or MAGNITUDE moves labelled there.


**Applies to:** empirical_strategy

### HARD-STRATEGY-02

Never assert a warrant bare: each IDENTIFICATION or IDENTIFYING_ASSUMPTION statement is paired, in the same or the next move, with the testable implication it yields, the institutional fact that supports it, or the check that will police it. Each threat raised gets an adjacent answer or an explicit route to one.

**Rationale.** Hedging an assumption is not defending it. The corpus defends by consequence and by check, and treats an unpoliced threat as an unfinished argument.

**Support.** 7/8 papers observable · share 0.88 · corpus 0.47 · 61 paragraphs

_Evidence._ 6 of 8 profiles pair warrants with implications or checks and 7 of 8 answer every threat they raise; the same rule reappears as a data-section and mechanism-section anti-pattern.


**Applies to:** empirical_strategy, data, mechanism, robustness

### HARD-ROBUST-01

Build every robustness check as PERTURBATION -> READOUT -> SCOPE VERDICT: name exactly what was changed, report the estimate at the main scale, then state what the survival or failure bounds. A readout without a scope verdict is incomplete.

**Rationale.** Robustness prose earns its place by saying what the check rules out, not by listing checks that were run.

**Support.** 9 papers · share 1.00 · corpus 0.60 · 69 paragraphs

_Evidence._ All 9 profiles with a robustness section; reinforced by the 9/9 requirement to close the section on a check outcome or handoff rather than on a stance claim.


**Applies to:** robustness

### HARD-ROBUST-02

Retire rivals inside the robustness section; never mint new ones. The section may name an identification threat or eliminate an alternative explanation, but it may not introduce a fresh claim that the body has not already supported.

**Rationale.** Robustness is where the corpus closes argument, and a new open question there reads as a leak rather than as a finding.

**Support.** 9 papers · share 1.00 · corpus 0.60 · 69 paragraphs

_Evidence._ 9 of 9 robustness profiles; MECHANISM moves are labelled zero times inside the robustness section in this corpus.


**Applies to:** robustness

### HARD-MECH-01

Keep channel statements below the inferential label of the design-identified average effect. A heterogeneity gradient, a targeting pattern, or a mediator correlation is reported at associational or suggestive-causal strength and never inherits the average effect's causal wording.

**Rationale.** This is the corpus's clearest epistemic boundary: heterogeneity is consistent with a mechanism, it does not demonstrate one.

**Support.** 8/10 papers observable · share 0.80 · corpus 0.53 · 118 paragraphs

_Evidence._ 8 of 10 mechanism profiles; the same prohibition appears independently in the results (5/10), robustness (9/9) and abstract (4/4) distillations.


**Applies to:** mechanism, results, robustness, abstract, conclusion

### HARD-MECH-02

Before reading any evidence as a channel, name the observation that separates the favoured channel from a rival - and give the channel claim its own evidentiary operation (a specification run for that channel, a subgroup or tail contrast, a component isolation, an explicit rival test).

**Rationale.** A mechanism paragraph without a discriminating operation is a restatement of the headline effect in different words.

**Support.** 8/10 papers observable · share 0.80 · corpus 0.53 · 118 paragraphs

_Evidence._ 8 of 10 mechanism profiles pair channel claims with an operation; 8 of 10 state the discriminating observation before the readout.


**Applies to:** mechanism

### HARD-DATA-01

Introduce a source before letting it carry argumentative weight: no dataset, register, survey wave, archive or self-built variable may be used as evidence in a paragraph until its provenance, coverage and construction are stated. Disclose each restriction (exclusions, window truncation, non-random availability, attrition) at the point that creates it.

**Rationale.** The data section is a warrant section. Provenance is what makes a later number interpretable, and a buried restriction is a defect in the reader's model of the estimate.

**Support.** 9/10 papers observable · share 0.90 · corpus 0.60 · 143 paragraphs

_Evidence._ 9 of 10 data profiles introduce sources before use; 7 of 10 disclose limits at the point of creation.


**Applies to:** data

### HARD-DATA-02

Hold provenance, coverage and definition statements unhedged, and put the section's hedging budget on interpretation and reach instead. Never hedge the warrant while asserting the reading.

**Rationale.** Documented facts do not deserve hedges, and hedges on them push the reader to distrust the measurement rather than the inference.

**Support.** 10 papers · share 1.00 · corpus 0.67 · 143 paragraphs

_Evidence._ All 10 data profiles hold the corpus's lowest hedge floor in this section and label zero strong-claim verbs there; the same placement rule recurs in institutional_background (8/10), conclusion (8/9) and abstract (4/4).


**Applies to:** data, institutional_background, results, robustness, conclusion, abstract

### HARD-BKGD-01

Include a piece of institutional context only if it has a downstream job: sourcing the variation, defining a measure or its population, stating a rule's threshold or date, or bounding a threat. Quantify the institution (date, threshold, coverage share, eligibility rule) instead of qualifying it.

**Rationale.** Background prose that nothing later cashes out reads as completeness, and the corpus spends its numbers on rules that carry the identification.

**Support.** 9/10 papers observable · share 0.90 · corpus 0.60 · 124 paragraphs

_Evidence._ 9 of 10 institutional-background profiles tie each paragraph to a downstream move; 7 of 10 quantify rather than qualify, and 9 of 10 keep literature positioning out of the section entirely.


**Applies to:** institutional_background

### HARD-CONCL-01

Keep verdict moves and scope moves in separate paragraphs: the paragraph that restates what was found may not also carry the caveat, and the paragraph that limits or generalizes may not introduce an estimate as fresh support.

**Rationale.** Mixing them makes the caveat read as a retreat from the finding and makes the finding read as unbounded.

**Support.** 9 papers · share 1.00 · corpus 0.60 · 147 paragraphs

_Evidence._ All 9 conclusion profiles separate verdict from scope; reinforced by the 9/9 rule that closing claims never exceed the strength the body assigned them.


**Applies to:** conclusion

### HARD-CONCL-02

Do not introduce a new estimand, outcome or test as a headline finding in the closer. Evidence re-delivered there arrives under a re-deployment label, and at least one answer-level move (a contribution restated as a differentiation, or a verdict tied to the named object) must be booked.

**Rationale.** The closer's job is to convert what was shown into a position, not to add a surprise result the reader cannot audit.

**Support.** 8/9 papers observable · share 0.89 · corpus 0.53 · 147 paragraphs

_Evidence._ 8 of 9 conclusion profiles forbid a new estimand; 9 of 9 book an answer-level move.


**Applies to:** conclusion

### HARD-LEX-01

Carry argumentative force with evidence labels and checks, not with intensifiers. In results, mechanism and robustness prose, verbs of proof (prove, demonstrate, establish, confirm) stay at or near zero; force comes from naming the design, the contrast and the check.

**Rationale.** Lexical assertiveness is the cheapest thing a draft can add and the least informative: it changes the sound of a claim without changing its warrant.

**Support.** 12/14 papers observable · share 0.86 · corpus 0.80 · 437 paragraphs

_Evidence._ Merged across results (9/10), robustness (8/9), mechanism (7/10) and data (10/10 strong-claim-verb floor); independent of the earlier section demotions.


**Applies to:** results, mechanism, robustness, data, empirical_strategy


**Exceptions:** Introductions and conclusions of model-led papers use framing verbs about what the theory delivers; the ceiling applies to empirical readouts.

## Strong Defaults

### DEF-INTRO-01

Close the introduction with a roadmap that names the remaining sections in the order their evidence is needed, rather than in file order.

**Rationale.** Readers use the roadmap to locate where each previewed claim is earned.

**Support.** 10/15 papers observable · share 0.67 · corpus 0.67 · 11 paragraphs

_Evidence._ 8 of 12 in introduction batch 1, 2 of 3 in batch 2.


**Applies to:** introduction

### DEF-INTRO-02

Place provenance (setting, data, measurement) before the results preview so the previewed number is attached to something the reader can already see.

**Rationale.** A preview without provenance floats.

**Support.** 10/12 papers observable · share 0.83 · corpus 0.67 · 15 paragraphs

_Evidence._ Introduction batch 1 only; the batch-2 pool was not scored for this behaviour, so the observable base is 12.


**Applies to:** introduction

### DEF-INTRO-03

Present design material in the introduction as an inventory - strategy named, assumption stated in counterfactual terms, confounders absorbed - and leave the proof to the strategy section.

**Rationale.** Introduction-length warrants invite the reader to over-read a preview as a defence.

**Support.** 8/15 papers observable · share 0.53 · corpus 0.53 · 8 paragraphs

_Evidence._ 7 of 12 in batch 1 plus 1 of 3 in batch 2.


**Applies to:** introduction

### DEF-INTRO-04

Position the paper's increment against the nearest prior work after the first preview, and state the delta in evidence or design rather than in novelty vocabulary.

**Rationale.** An increment claimed before the finding is a promise; after the finding it is a comparison.

**Support.** 9/12 papers observable · share 0.75 · corpus 0.60 · 9 paragraphs

_Evidence._ Introduction batch 1; not observable in the batch-2 pool as scored.


**Applies to:** introduction, literature

### DEF-INTRO-05

Pre-empt at least one rival reading inside the introduction, even if only to leave attribution explicitly open.

**Rationale.** Naming the rival before the design claims to have excluded it signals that the design was built with the rival in mind.

**Support.** 8/14 papers observable · share 0.57 · corpus 0.53 · 10 paragraphs

_Evidence._ 7 of 12 in batch 1 as an inventory behaviour, 1 of 3 in batch 2 as an explicit default.


**Applies to:** introduction

### DEF-RESULT-01

Reopen SPECIFICATION whenever the estimand, outcome set, sample restriction, or fixed-effect and clustering structure changes, so each new number arrives with its own object.

**Rationale.** Silent re-specification is how a results section starts to look like a pile of coefficients.

**Support.** 7 papers · share 1.00 · corpus 0.47 · 41 paragraphs

_Evidence._ All 7 results profiles that report more than one estimand.


**Applies to:** results

### DEF-RESULT-02

Restate the headline at least twice with a different evidence angle between the repetitions (a specification change, a validation display, a magnitude translation).

**Rationale.** Repetition with changed angles is how the corpus builds confidence without repeating a claim.

**Support.** 8/10 papers observable · share 0.80 · corpus 0.53 · 60 paragraphs

_Evidence._ 8 of 10 results profiles; note the direct conflict with the robustness rule against re-arguing the main result, resolved as section-scoped.


**Applies to:** results


**Exceptions:** Robustness sections: the same restatement there is an anti-pattern.

### DEF-RESULT-03

Close the results section on evidence - MAIN_RESULT, MAGNITUDE, ROBUSTNESS or NULL_RESULT - and move limitations and interpretive wrap-ups to their own sections.

**Rationale.** Ending on a caveat makes the section read as an apology for its own numbers.

**Support.** 9/10 papers observable · share 0.90 · corpus 0.60 · 250 paragraphs

_Evidence._ 9 of 10 results profiles.


**Applies to:** results

### DEF-ABSTRACT-01

Write the abstract as one block carrying one governing move, sequenced as: what the paper interrupts, the device that makes it answerable, the verdict. Include the answer, not only the question, and at most one translated magnitude.

**Rationale.** Abstracts in this corpus are compressed result arcs; the ones that read as background summaries fail to differentiate the paper.

**Support.** 4 papers · share 1.00 · corpus 0.27 · 5 paragraphs

_Evidence._ All 4 abstract profiles. Observable base is 4 of 15 papers, so this stays a default despite unanimity.


**Applies to:** abstract

### DEF-ABSTRACT-02

Keep citations and prior-work summaries out of the abstract; positioning belongs to the introduction.

**Rationale.** Reference work in an abstract spends the space that would carry the finding.

**Support.** 4 papers · share 1.00 · corpus 0.27 · 5 paragraphs

_Evidence._ 4 of 4 abstract profiles.


**Applies to:** abstract

### DEF-LIT-01

Organise the literature by research strand, and state for each strand what it measures or assumes and what its evidence can and cannot support.

**Rationale.** Strand-level claims give the design something to respond to; author-by-author recaps do not.

**Support.** 3 papers · share 1.00 · corpus 0.20 · 18 paragraphs

_Evidence._ 3 of 3 literature profiles; base is too thin for a hard rule.


**Applies to:** literature

### DEF-LIT-02

Claim entry only after naming a documented gap, contradiction, or measurement that did not previously exist.

**Rationale.** Absence alone is not a contribution claim; what the absence blocked is.

**Support.** 3 papers · share 1.00 · corpus 0.20 · 18 paragraphs

_Evidence._ 3 of 3 literature profiles.


**Applies to:** literature

### DEF-CONCL-01

State limitations as scope conditions on the design's warrant and pair each with what would lift it (a data object, an institution, a contrast).

**Rationale.** A limitation without a route reads as a shrug; with one it reads as a boundary.

**Support.** 6/9 papers observable · share 0.67 · corpus 0.40 · 12 paragraphs

_Evidence._ 6 of 9 conclusion profiles.


**Applies to:** conclusion

### DEF-CONCL-02

Keep closer numbers to translated magnitudes, comparisons and counts; no test statistics, standard errors, or table and column pointers.

**Rationale.** The closer argues from meaning, not from apparatus.

**Support.** 7/9 papers observable · share 0.78 · corpus 0.47 · 147 paragraphs

_Evidence._ 7 of 9 conclusion profiles.


**Applies to:** conclusion

### DEF-DATA-01

Use ROADMAP moves inside the data section to mark a change of object (source, then measure, then design, then check), never to preview findings.

**Rationale.** Intra-section signposts keep a long measurement argument readable without turning it into a results teaser.

**Support.** 8/10 papers observable · share 0.80 · corpus 0.53 · 143 paragraphs

_Evidence._ 8 of 10 data profiles.


**Applies to:** data

### DEF-MECH-01

Put the hedge on the attribution sentence rather than on the channel readout: report the channel estimate with its apparatus unhedged and mark the inferential step as suggestive.

**Rationale.** Hedging the number hides imprecision that the apparatus already states; hedging the attribution is where the uncertainty actually lives.

**Support.** 7/10 papers observable · share 0.70 · corpus 0.47 · 118 paragraphs

_Evidence._ 7 of 10 mechanism profiles.


**Applies to:** mechanism

## Optional Styles

### OPT-INTRO-01

Run THEORY slots inside the introduction before the empirical turn - as an assumption stack the later algebra must deliver, or as a sign-ambiguous case split that licenses the empirical pivot.

**Rationale.** Legitimate for structural or theory-driven designs; seven of twelve profiles in one batch are purely reduced-form and do without.

**Support.** 5/12 papers observable · share 0.42 · corpus 0.33 · 9 paragraphs

_Evidence._ paper02, paper04, paper06, paper07, paper12.


**Applies to:** introduction

### OPT-INTRO-02

Open on a literature-as-foil paragraph rather than on the phenomenon, then pivot to the gap.

**Rationale.** Observed in positioning-led entries; contradicted by one batch's anti-pattern, so it is a stylistic option chosen by some papers, not a corpus policy.

**Support.** 3/12 papers observable · share 0.25 · corpus 0.20 · 3 paragraphs

_Evidence._ Introduction batch 1, LITERATURE_POSITION-led openers.


**Applies to:** introduction

### OPT-INTRO-03

Deliver the identification material as a single inventory paragraph ahead of the preview, or split it across the design and assumption paragraphs.

**Rationale.** Both shapes appear with equal success; the choice is about how much of the warrant the introduction should carry.

**Support.** 7/12 papers observable · share 0.58 · corpus 0.47 · 8 paragraphs

_Evidence._ Introduction batch 1.


**Applies to:** introduction

### OPT-ABSTRACT-01

Write a contribution-only abstract with no data, no design detail and no numbers.

**Rationale.** Observed in one profile; consistent with the section's verdict requirement but unusual in this corpus.

**Support.** 1/4 papers observable · share 0.25 · corpus 0.07 · 1 paragraphs

_Evidence._ Single profile.


**Applies to:** abstract

### OPT-CONCL-01

Reopen the paper's own question in the closer and answer it there, instead of opening the closer on the answer.

**Rationale.** Question-in/question-out framing appears in a minority of closers and reads well when the question was posed instrumentally.

**Support.** 3/9 papers observable · share 0.33 · corpus 0.20 · 3 paragraphs

_Evidence._ Conclusion batch 1.


**Applies to:** conclusion

### OPT-CONCL-02

Close on an explicit research agenda hand-off - open items plus the data each would require - rather than on a limitation paragraph.

**Rationale.** Used by papers whose contribution is a new measurement object.

**Support.** 3/9 papers observable · share 0.33 · corpus 0.20 · 3 paragraphs

_Evidence._ Conclusion batch 1.


**Applies to:** conclusion

### OPT-CONCL-03

Let closer length vary freely: a two-move verdict-then-limit closer and a fourteen-move closer that also hosts specification and validation are both attested.

**Rationale.** Length carries no section norm in this corpus.

**Support.** 9 papers · share 1.00 · corpus 0.60 · 147 paragraphs

_Evidence._ All conclusion profiles; recorded as optional precisely because it prescribes nothing.


**Applies to:** conclusion

### OPT-RESULT-01

Pair two estimands in one ladder (measure, readout, robustness, measure, readout) when the paper's claim depends on both.

**Rationale.** A structural variant of the report-then-translate cadence.

**Support.** 2/10 papers observable · share 0.20 · corpus 0.13 · 6 paragraphs

_Evidence._ Introduction batch 2 grammar plus one results profile.


**Applies to:** results

### OPT-DATA-01

Merge the data and identification arguments into one section when there is no dedicated strategy section, sequencing threat, assumption, identification, validation, specification.

**Rationale.** Used by papers whose identification is measurement-driven.

**Support.** 3/10 papers observable · share 0.30 · corpus 0.20 · 22 paragraphs

_Evidence._ Data-section grammar observed in three profiles.


**Applies to:** data, empirical_strategy

### OPT-BKGD-01

End the background on a handoff paragraph that converts description into argumentative currency (data, measurement, identification) rather than on a summary of the institution.

**Rationale.** Observed in the stronger backgrounds; a summary close leaves the reader to find the hook.

**Support.** 8/10 papers observable · share 0.80 · corpus 0.53 · 124 paragraphs

_Evidence._ 8 of 10 institutional-background profiles; recorded as optional because a handoff can equally be the first line of the next section.


**Applies to:** institutional_background

### OPT-LEX-01

Vary register freely on nominalization, semicolon chaining and parenthetical density; none of these track section norms in this corpus.

**Rationale.** Recorded so the critic does not flag a legitimate authorial voice as an error.

**Support.** 15 papers · share 1.00 · corpus 1.00 · 1178 paragraphs

_Evidence._ Section metric spreads show the full range within every section type.


**Applies to:** data, results, conclusion, mechanism

## Anti-patterns

### AP-INTRO-01

Opening the introduction on the sample, the estimator or the headline number.

**Rationale.** Forces the reader to evaluate machinery with no question in mind.

**Support.** 15 papers · share 1.00 · corpus 1.00 · 15 paragraphs

_Evidence._ Absent from all 12 batch-1 and all 3 batch-2 introductions.


**Applies to:** introduction

### AP-INTRO-02

Booking the contribution with evaluative novelty vocabulary (first to study, novel setting, extends the literature) without naming the closest prior work and the specific delta.

**Rationale.** Novelty words are cheap; the corpus earns the claim with a stated departure.

**Support.** 9/12 papers observable · share 0.75 · corpus 0.60 · 9 paragraphs

_Evidence._ Introduction batch 1 (6/12) and batch 2 (3/3).


**Applies to:** introduction, conclusion, abstract

### AP-INTRO-03

Reporting an introduction estimate with its statistical apparatus attached - standard errors in parentheses, full specification notation.

**Rationale.** The introduction gives the quantity and its interpretation; results give the apparatus.

**Support.** 3 papers · share 1.00 · corpus 0.20 · 3 paragraphs

_Evidence._ Introduction batch 2 only; the batch-1 pool was not scored for it.


**Applies to:** introduction

### AP-CLAIM-01

Promoting a channel, mediator or heterogeneous-response observation to causal-strength wording because it is consistent with the headline effect, or using a null as positive disproof of a rival.

**Rationale.** The corpus's most important epistemic boundary; the strongest single cross-section regularity after warrant grading.

**Support.** 13/14 papers observable · share 0.93 · corpus 0.87 · 210 paragraphs

_Evidence._ Merged across results (5/10), mechanism (6/10), robustness (9/9), abstract (4/4) and conclusion (7/9).


**Applies to:** mechanism, results, robustness, abstract, conclusion

### AP-CLAIM-02

Distributing hedges evenly across a section so that design, measurement and result sentences are softened as much as interpretive ones - or substituting sentence-level hedging for the assumption or precision statement that would justify it.

**Rationale.** Even hedging destroys the signal hedging is supposed to carry.

**Support.** 12/14 papers observable · share 0.86 · corpus 0.80 · 300 paragraphs

_Evidence._ Merged hedge-placement prohibitions from introduction, data, institutional_background, mechanism, empirical_strategy and conclusion.


**Applies to:** introduction, data, empirical_strategy, mechanism, institutional_background, conclusion

### AP-RESULT-01

Carrying causal force with intensifying verbs (prove, demonstrate, establish, confirm) in results prose.

**Rationale.** Force belongs to the evidence label and the check, not the verb.

**Support.** 9/10 papers observable · share 0.90 · corpus 0.60 · 250 paragraphs

_Evidence._ 9 of 10 results profiles hold strong-claim-verb rates at or near zero.


**Applies to:** results, robustness, mechanism

### AP-RESULT-02

Reporting a bare coefficient as the section's contribution with no comparable-unit translation and no internal or literature comparator.

**Rationale.** Without a translation the reader cannot weigh the result.

**Support.** 8/10 papers observable · share 0.80 · corpus 0.53 · 74 paragraphs

_Evidence._ 8 of 10 results profiles.


**Applies to:** results

### AP-RESULT-03

Doing literature work inside estimate paragraphs, or opening and closing the results section with positioning, contribution or policy-relevance material.

**Rationale.** Positioning has its own slots; estimate paragraphs are where the corpus stays on its own evidence.

**Support.** 10 papers · share 1.00 · corpus 0.67 · 250 paragraphs

_Evidence._ All 10 results profiles.


**Applies to:** results

### AP-ROBUST-01

Re-arguing the main result in the robustness section - restating its substantive interpretation, re-running the motivation, or presenting a surviving check as a fresh finding.

**Rationale.** The section's job is bounding, not persuading again.

**Support.** 9 papers · share 1.00 · corpus 0.60 · 69 paragraphs

_Evidence._ All 9 robustness profiles. Note the deliberate asymmetry with results, where headline restatement is a default.


**Applies to:** robustness

### AP-ROBUST-02

Reporting only the checks that pass, or letting a battery contain no threat, no null and no conceded untestable case.

**Rationale.** The corpus treats an all-clear battery as incomplete reporting rather than as clean evidence.

**Support.** 6/9 papers observable · share 0.67 · corpus 0.40 · 6 paragraphs

_Evidence._ 6 of 9 robustness profiles.


**Applies to:** robustness

### AP-DATA-01

Letting provenance do the work of identification - describing where data came from, how many records it holds, or that a rule was officially promulgated - as if availability licensed a causal reading.

**Rationale.** Data availability is not identification; the corpus keeps these warrants separate.

**Support.** 10 papers · share 1.00 · corpus 0.67 · 143 paragraphs

_Evidence._ All 10 data profiles; reinforced by the data section's zero strong-claim-verb floor.


**Applies to:** data, institutional_background

### AP-DATA-02

Burying a known restriction in a footnote or appendix, or delivering a variable and control inventory without saying what each term absorbs.

**Rationale.** The reader's model of the estimate is set by what the section discloses where it applies.

**Support.** 7/10 papers observable · share 0.70 · corpus 0.47 · 143 paragraphs

_Evidence._ 7 of 10 data profiles disclose at point of creation; 2 of 10 show the inventory anti-pattern directly.


**Applies to:** data

### AP-STRATEGY-01

Defending an identifying assumption by restating the model, by asserting plausibility, or by citation volume.

**Rationale.** Precedent licenses the choice of estimator; it does not license the assumption.

**Support.** 8 papers · share 1.00 · corpus 0.53 · 75 paragraphs

_Evidence._ All 8 empirical-strategy profiles; 6 of 8 also forbid design claims supported by citation counts.


**Applies to:** empirical_strategy

### AP-STRATEGY-02

Merging what varies with what must hold - one undifferentiated assertion covering both the source of variation and the identifying assumption.

**Rationale.** Readers need to know which part the design supplies and which part the argument must defend.

**Support.** 6/8 papers observable · share 0.75 · corpus 0.40 · 6 paragraphs

_Evidence._ 6 of 8 empirical-strategy profiles.


**Applies to:** empirical_strategy

### AP-CONCL-01

A section-by-section recap in source order (data, then strategy, then results, then robustness) instead of argument-level moves.

**Rationale.** The closer converts findings into a position; a replay of structure adds nothing.

**Support.** 8/9 papers observable · share 0.89 · corpus 0.53 · 147 paragraphs

_Evidence._ 8 of 9 conclusion profiles.


**Applies to:** conclusion

### AP-CONCL-02

Policy advocacy in the closer or abstract - claims about what agencies will or should do, presented as findings.

**Rationale.** The corpus states conditional implications of its own evidence and disclaims process claims.

**Support.** 9/13 papers observable · share 0.69 · corpus 0.60 · 12 paragraphs

_Evidence._ Merged from conclusion (3/9) and abstract (4/4) and introduction (2/12) prohibitions.


**Applies to:** conclusion, abstract, introduction

### AP-LIT-01

Citation catalogue: a paragraph structured as 'A does X, B does Y, C does Z' with no strand-level claim and no consequence for the design; or a novelty claim resting only on 'no prior study has done X'.

**Rationale.** Positioning has to say what the absence blocked, and what the paper's design does differently.

**Support.** 3 papers · share 1.00 · corpus 0.20 · 18 paragraphs

_Evidence._ All 3 literature profiles; base is too thin for a hard rule.


**Applies to:** literature

### AP-GEN-01

Unhedged generalization in final position, or a reach statement whose warrant comes from a different setting than the one sampled.

**Rationale.** The corpus puts its hedging on reach; a wide unqualified claim reads as an error of the very discipline the rest of the paper maintains.

**Support.** 9 papers · share 1.00 · corpus 0.60 · 147 paragraphs

_Evidence._ All 9 conclusion profiles; the mirrored requirement appears in the abstract and introduction distillations.


**Applies to:** conclusion, abstract