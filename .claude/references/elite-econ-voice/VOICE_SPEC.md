# Elite Empirical Economics Voice Specification

**Version:** 1.0.0  
**Authority:** This file is the authoritative source for the Elite Economics Voice layer.  
**Scope:** linguistic realization only. It cannot override evidence, identification, the Scientific Style Bundle, or manuscript content invariants.

## Precedence

1. actual data/results/citations;
2. content invariants and identification fidelity;
3. Scientific Style Bundle claim-evidence rules and HARD rules;
4. this Elite Economics Voice specification;
5. optional personal preferences;
6. generic Clo-Author prose defaults.

When a voice rule would strengthen a claim beyond the scientific-style permission, ignore the voice rule.

---

## Voice Signatures

### EV-SIG-01 — Use explicit research-agent syntax when the action matters

Prefer an explicit actor and a specific research verb for data construction, design, estimation, and discovery: *we use, construct, exploit, estimate, find, document, show, test*. Do not hide a consequential research action behind an empty passive merely to sound formal.

**Support:** 6/6 source-author strata.  
**Applies to:** abstract, introduction, data, empirical_strategy, results, mechanism.

### EV-SIG-02 — Put a concrete research object early in the sentence

Open substantive sentences with the phenomenon, object, sample, comparison, design, estimate, or implication. Avoid dummy openings whose only function is to announce that something is important or about to be discussed.

**Support:** 6/6.  
**Applies to:** all prose sections.

### EV-SIG-03 — Let the verb encode the epistemic job

Use different verbs for different jobs:
- *study/examine* for the question;
- *use/construct* for data or measures;
- *exploit/randomize/instrument* for design;
- *estimate* for quantities;
- *find* for empirical results;
- *document* for descriptive facts/patterns;
- *show* only when the evidence supports a direct statement;
- *suggest/is consistent with* for interpretation or mechanism evidence below direct-test strength.

Do not use synonyms merely to avoid repetition if they blur the evidentiary role.

**Support:** 6/6.  
**Applies to:** all empirical sections.

### EV-SIG-04 — Integrate important quantities into the substantive sentence

When a magnitude matters, place it in the same sentence as the object it quantifies or in an immediately adjacent translation sentence. Prefer interpretable comparisons to naked coefficients.

**Support:** 6/6.  
**Applies to:** abstract, introduction preview, results, conclusion.

### EV-SIG-05 — Build comparisons with matched contrastive syntax

When two objects are the point of the argument, put them into visibly parallel syntax: treated versus control, before versus after, high versus low, one mechanism versus another. Use *but, while, whereas, in contrast,* or similarly compact connectors rather than a long transition preamble.

**Support:** 6/6.  
**Applies to:** introduction, results, mechanism, robustness, discussion.

### EV-SIG-06 — Localize hedging to the inferential step

State documented facts, design operations, sample definitions, and estimates directly. Put uncertainty on mechanism attribution, interpretation, extrapolation, and rival explanations. Do not soften every sentence equally.

**Support:** 6/6.  
**Applies to:** all sections; subordinate to Scientific Style claim-evidence rules.

### EV-SIG-07 — Compress method sentences around purpose

A strong method bridge usually answers three things without digression: what variation/object is used, what action is taken, and what that action identifies or distinguishes. Prefer compact patterns such as *Using X, we estimate Y* or *To distinguish A from B, we exploit Z* when accurate.

**Support:** 5/6.  
**Applies to:** introduction, data, empirical_strategy, mechanism.

### EV-SIG-08 — Make clause order mirror research logic

Order clauses so the reader can reconstruct the argument without backtracking. Common linear orders are:
- premise → action → result;
- source of variation → estimator/test → estimand;
- result → magnitude/comparator → interpretation;
- rival → discriminating prediction → test → bounded verdict.

Avoid ornamental nesting that delays the main verb or reverses the evidentiary sequence.

**Support:** 6/6.  
**Applies to:** all prose sections.

### EV-SIG-09 — Use comparators to make magnitudes legible

Whenever feasible, translate a headline quantity against a pre-period mean, control-group mean, baseline probability, standard deviation, alternative estimate, or economically meaningful benchmark.

**Support:** 6/6.  
**Applies to:** abstract, introduction, results, conclusion.

### EV-SIG-10 — Close paragraphs on inference, boundary, or handoff

After evidence, end with what the evidence changes: an interpretation at the licensed strength, a bound, a contrast, a threat resolved, or a handoff to the next analytic object. Avoid generic summary closers.

**Support:** 5/6.  
**Applies to:** introduction, results, mechanism, robustness, conclusion.

---

## Strong Defaults

### EV-DEF-01 — Prefer functional first person over ceremonial impersonality

Use *we* when it makes the research action clearer. Avoid converting *we estimate* into *it is estimated* solely to sound academic.

**Support:** 6/6.

### EV-DEF-02 — Name the research question directly

Preferred forms are a direct question/puzzle or a sentence such as *We study whether/how...*. Avoid *The aim of this paper is to...* unless the sentence immediately names a precise object and cannot be shortened.

**Support:** 5/6.

### EV-DEF-03 — Use "find" economically

*We find* is a workhorse, not a signature phrase. Use it for the main empirical readout, then vary by function (*document, estimate, show, suggest, imply*) rather than thesaurus substitution.

**Support:** 6/6.

### EV-DEF-04 — Enumerate only genuinely separate findings

*First/Second/Third* is useful when the reader must keep distinct empirical facts, predictions, or mechanisms apart. Do not manufacture a three-part list for cadence.

**Support:** 5/6.

### EV-DEF-05 — Prefer simple contrast markers

Use *however, but, while, whereas, in contrast* when the semantic relation is genuinely contrastive. Avoid multiword transitions that merely announce a pivot.

**Support:** 6/6.

### EV-DEF-06 — Put citations next to propositions, not around them

A literature sentence should first make a claim about what prior work establishes, assumes, or measures; citations support that proposition. Avoid author-by-author catalogues unless chronology or disagreement is itself the object.

**Support:** 5/6.

### EV-DEF-07 — Let one connective do one job

Do not stack *however, moreover, in addition, importantly* at paragraph boundaries. If the logical relation is clear from sentence content, no transition word is required.

**Support:** 5/6.

### EV-DEF-08 — Alternate density rather than enforce uniform sentence length

Dense sentences are acceptable for tightly linked design logic. Follow them with a cleaner sentence when a result, implication, or contrast deserves emphasis. Do not optimize every sentence to the same length.

**Support:** 6/6; no hard word-count target inferred.

### EV-DEF-09 — Open result paragraphs with the substantive object

Prefer a result, estimand, or contrast over *Table 3 reports...*. Table/figure references can follow the claim.

**Support:** 5/6.

### EV-DEF-10 — State caveats plainly

When a limitation matters, name the precise scope or identifying dependency. Avoid apologetic language, diffuse hedging, or generic "limitations remain."

**Support:** 6/6.

---

## Voice Options

These are legitimate ensemble variants and are never scored as requirements.

### EV-OPT-01 — Question-led introduction

A paper may open with a direct large question when the question itself is concrete and immediately tied to an empirical object.

### EV-OPT-02 — Direct declarative versus "we" opening

Both *X increased Y* and *We find that X increased Y* are acceptable when scientific-style claim strength permits the statement.

### EV-OPT-03 — Explicit numbered findings

Numbered findings can clarify a genuinely multi-result paper, especially in abstracts and introduction previews, but are not a default skeleton.

### EV-OPT-04 — Long argumentative sentence

A long sentence is acceptable when clauses have transparent logical relations and the main verb arrives early enough to prevent backtracking.

### EV-OPT-05 — Sparse transition prose

A paragraph may begin without any connective when the semantic relation to the previous paragraph is already obvious.

---

## Voice Avoidances

### EV-AVOID-01 — Metadiscursive throat-clearing

Avoid phrases whose main job is announcing significance rather than carrying content: *it is important to note, it is worth noting, it is interesting to observe, in today's rapidly changing...*

### EV-AVOID-02 — Evaluative adverbs as substitutes for evidence

Use *importantly, notably, remarkably, crucially* sparingly. If the fact is important, the object, magnitude, or comparison should usually make that visible.

### EV-AVOID-03 — Mechanical "we find that" repetition

Do not begin consecutive sentences with the same reporting frame when the rhetorical jobs differ.

### EV-AVOID-04 — Transition stacking

Avoid paragraph openings such as *Moreover, importantly, in addition...* or repeated *Furthermore/Additionally* chains.

### EV-AVOID-05 — Passive voice that obscures agency

Do not write *it is shown/it is found/it is estimated* when the active sentence would clarify the research action without changing meaning.

### EV-AVOID-06 — Ornamental synonym substitution

Do not replace a precise economics verb with a grander near-synonym to sound sophisticated. Precision beats lexical variety.

### EV-AVOID-07 — Topic-word imitation

Do not copy recurring content vocabulary from source authors (e.g., their favored institutions, technologies, or political-economy objects) into unrelated papers.

### EV-AVOID-08 — Signature-phrase imitation

Do not reproduce memorable source wording, metaphors, or idiosyncratic phrasings. This bundle transfers structure and linguistic choices, not recognizable expressions.

### EV-AVOID-09 — Generic significance closers

Avoid *These findings have important implications*, *This highlights the importance of*, or *This provides valuable insights* unless the sentence immediately specifies the exact implication and can be rewritten more directly.

### EV-AVOID-10 — Apparatus-heavy prose when meaning is available

Do not let column numbers, standard errors, estimator labels, or specification names replace an interpretable statement of what changed and by how much.
