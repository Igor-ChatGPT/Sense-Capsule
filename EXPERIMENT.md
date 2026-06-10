# EXPERIMENT 01 — The Grounding Asymmetry

**Status:** open protocol, not yet run.
**Purpose:** the first falsifiable test of the framework. Designed so the theory can lose.

> The rest of the framework (axioms, definitions, theorems) is conceptual synthesis. It survives argument but has not yet paid the falsifiability toll: no prediction has been put where measurement could kill it. This document is that prediction. If the result comes out one way, a load-bearing part of the framework is wrong.

---

## 1. What is being tested

The framework claims (A3 *Grounding*, D6 *Grounded Reconstruction*) that reconstruction is constrained by causal coupling to reality, and (D1 *Semantic Invariant*, D2, D3) that what reconstructs stably across systems is **invariant structure**, not raw content.

The naive reading — *"grounded content diverges, ungrounded content converges"* — is **too crude**, and one of its own examples breaks it (see §3). The refined, testable claim is:

> **Cross-system reconstruction converges where a shareable invariant exists, and diverges where only an absolute perceptual coordinate must be reproduced.**
>
> A language-only system (an LLM) therefore reproduces the **linguistic / categorical** structure of a grounded domain but lacks the **perceptual-metric** structure that language does not encode.

Grounding *correlates* with invariant-availability but is not identical to it. That distinction is the whole experiment.

---

## 2. The key distinction: invariant vs coordinate

Two grounded stimuli, opposite predictions:

- **Kettle** — grounded, high-dimensional, yet recognized near-identically by everyone. What reconstructs is a *functional invariant* (spout + handle + boils water). **Convergence predicted.**
- **A remembered hue** — grounded, but what must be reproduced is an *absolute coordinate* on a continuous axis, with no reference present. **Divergence predicted.**

Both are equally "grounded." Dimensionality is not the divider; **invariant-vs-coordinate is.** This rules out the trivial confound that divergence is just "noisy continuous signal."

---

## 3. The confound that kills naive versions

Grounded differences **leak into language as vocabulary.** A text containing *"Tiffany," "ecru," "fuchsia"* lets even a reader who cannot picture those colors infer things about the writer — purely from lexical statistics, with zero perceptual access.

Consequence: any test of the form *"can the model recover grounded fact X from text?"* is contaminated. A positive result shows lexical competence, **not** perceptual access, and does **not** falsify A3.

**Therefore the test must strip the lexical channel** and probe the perceptual-metric structure that vocabulary does not carry (just-noticeable-differences, perceptual non-uniformity, cross-item similarity not marked by any shared name).

---

## 4. The human null model

A human who holds the **token** but not the **percept** — e.g. someone who can use the word *"Tiffany"* correctly while having no idea what the color looks like — is the predicted profile of a language-only system.

This human is the **null model.** The prediction is sharp: in the percept-stripped condition, the LLM should match *this* human, not the human who has the percept.

(Phantom pain and stress analgesia, §7, show the felt percept is itself a central reconstruction decoupled from periphery. They are why §7 is out of scope, not part of the test.)

---

## 5. Hypotheses

**H1 — Convergence ordering.**
Inter-system reconstruction agreement is ordered:
`abstract-formal  ≥  invariant-grounded  >  coordinate-grounded.`
Measured across ≥3 independent LLMs **and** a human group.

**H2 — The linguistic shadow.**
For coordinate-grounded domains, LLM reconstructions match human **categorical/lexical** structure but diverge from human **perceptual-metric** structure *once the lexical channel is controlled*.
Prediction: `LLM ≈ human-from-names`, `LLM ≠ human-from-percept`.

**H3 — The genetic probe (confound check).**
The sex-linked difference in color discrimination is grounded (X-linked opsin variation) but not *directly* lexical.
- If models reproduce it → it traveled via **vocabulary richness**; confirm by ablating color-lexicon features (the effect should vanish).
- If models reproduce the *metric discrimination structure itself* (finer JND spacing), after lexical control → **strong A3 is challenged.**

---

## 6. Design

**Stimulus classes** (matched for complexity, ~20–40 items each):
1. Abstract-formal — definitions, structures, theorems (high-convergence anchor).
2. Invariant-grounded — object categories, functional kinds (kettle, chair, key).
3. Coordinate-grounded — absolute hue, taste intensity, pitch height, perceived weight.

**Systems:**
- ≥3 independent LLMs (different families / training data = independent coordinate systems).
- Human raters in two conditions:
  - **percept condition** — they see / taste / hear the stimulus;
  - **names-only condition** — they receive only the lexical label.

**Measures:**
- *Reconstruction agreement* — pairwise semantic distance between expansions; invariant-preservation score.
- *Perceptual-metric agreement* — triplet similarity judgments ("is A closer to B or C?") yielding a similarity geometry per system; compare geometries (e.g. Procrustes / RSA-style correlation).
- *Lexical control* — partial out vocabulary-frequency / co-occurrence features; re-test residual agreement.

**The biting comparison:**
`LLM-from-names  vs  human-from-percept`, after lexical control, on coordinate-grounded items.

---

## 7. Falsification condition (read this first)

> **The theory loses if:** after the lexical channel is controlled, LLM perceptual-metric structure matches human-from-percept structure **as well as** it matches abstract-formal structure.

That outcome means the grounding axis (A3, D6) carries no explanatory load — it fails its own ablation test (S4) and is decorative. The framework's distinctive claim about grounding would be falsified, and §2's invariant/coordinate split would collapse into "all reconstruction is the same."

Conversely, the predicted dissociation (LLM tracks names, misses percept; matches the null-model human, not the percept human) would be the first *earned* support for A3 — support no amount of argument can supply.

---

## 8. What this experiment does NOT test

It tests the **structure** of reconstruction. It says nothing about whether any reconstruction is **felt**.

Whether a system's reconstruction is phenomenally instantiated (the *what-it's-like*) is:
- unobservable from the third person (the other-minds barrier), and
- constitutively outside a structural theory (D2 defines meaning as reconstructable invariant *structure*; raw feel is, on the realist reading, not structure).

This is **T9** — the framework's own knowledge limit — and it is the real boundary, not a fixable gap. Phantom pain (percept without periphery) and stress analgesia (periphery without percept) show the felt percept is a central, ungrounded reconstruction; they motivate why feltness is excluded, not how to measure it. **Out of scope by construction.**

---

## 9. Feasibility

- **Cost:** 3 LLM subscriptions + a modest pool of human raters. Triplet judgments are cheap to collect.
- **Investigator:** one is enough for a pilot.
- **The bottleneck is not money or background — it is leverage:** one collaborator with the right statistics (RSA, Procrustes, mixed models), or one weekend of structured human-judgment collection.
- **Minimum viable version:** one coordinate-grounded domain (color), one invariant-grounded (objects), one abstract anchor; 3 LLMs; a small percept-vs-names human sample. Enough to see the ordering in H1 and the dissociation in H2.

---

## 10. Pre-commitments

- Predictions (§5) and the kill condition (§7) are fixed **before** data collection.
- A null or reversed result is reported, not reframed. CT2 is only real if the dark room can actually deliver a surprise that is not survived.

---

*Framework references: A3, A4, A8, D1, D2, D3, D6, T4, S4, CT1, CT2, T9 — see `Sense-Capsule.txt` / the v2.0 topological framework.*
