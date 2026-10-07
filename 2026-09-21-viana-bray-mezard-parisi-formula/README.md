# The Mézard–Parisi formula for the Viana–Bray model

**Integrated edition: September 21, 2026 (Pacific time), 46 pages.** This folder preserves an AI-generated research manuscript developed through user-guided review and revision. The historical PDF is unchanged.

**Audit status: proposed proof; complete verification remains pending.** The latest scope and hypothesis review did not demonstrate a mathematical gap or invalid inference in this edition. That limited review does not establish that the entire proof is correct or error-free.

## Claimed result and proof approach

Theorem 1.1 claims the Mézard–Parisi variational formula for the limiting quenched free energy of the Viana–Bray model, for every fixed finite connectivity and inverse temperature, a fixed dimensionless external field, and a **bounded symmetric coupling distribution**. The variational infimum is over finite-depth Ruelle probability cascade trials with a deterministic measurable message function and independent site-mark trees. The depth can grow; the statement does not require a finite number of replica-symmetry-breaking levels to attain the infimum.

The manuscript combines the interpolation upper bound with a proposed reverse inequality. Its route constructs a stationary spin law with the required cavity value, minimizes a Poissonized cavity functional, and enriches the law with canonical cluster centres and marked Ghirlanda–Guerra identities. It then uses a common hierarchy and conditional row independence to recover the spin law and cavity value through consistent finite cascade approximations.

This is a finite-temperature statement with bounded couplings. Extensions beyond those hypotheses require additional arguments.

## When this edition was obtained

The recovered September 21, 2026 conversation records the following sequence. All times below are **Pacific daylight time (UTC−7)** and are recorded assistant-response completion times.

| Time | Recorded output |
| --- | --- |
| 3:00 p.m. | Favorable AI audit of an uploaded 59-page precursor: a 40-page manuscript and a 19-page expanded-proof supplement. |
| 3:29 p.m. | A single integrated 45-page paper, placing the expanded arguments into the main text and unifying the exposition. |
| 3:57 p.m. | A 46-page revision of Sections 1.4–1.5. |
| 10:48 p.m. | A further revision of Section 1.5 explaining the cancellation and branch-independence mechanisms. |

The archived PDF's creation metadata is September 21 at 10:46:59 p.m. PDT (September 22 at 05:46:59 UTC), consistent with the final revision. Metadata and conversation timestamps are different records. The PDF has no printed manuscript date. The same 46-page edition was attached again in a comparison conversation on October 6.

These records date the integrated edition, **not the first discovery of its underlying argument**. The recovered conversation begins with an existing 59-page manuscript. It does not establish public priority.

## How it was generated

**Iterative AI proof development under human direction, rather than a one-shot finished proof.** In the recovered conversation, the user supplied the existing manuscript, requested a critical audit, then requested integration and clearer explanations. The assistant audited the precursor and produced successive integrated and expository revisions.

That conversation contains one audit response and three integration or exposition revision responses. The original September 20 research brief has now been recovered and is preserved below; the complete sequence of intervening proof-development responses has not been reconstructed here. These are visible responses, not a count of all model calls or a complete account of how the original proof strategy arose.

## Original research prompt

The original proof-generation brief comes from the **September 20, 2026 (Pacific time)** development chat. The full text is preserved **verbatim** in [ORIGINAL-PROMPT.txt](ORIGINAL-PROMPT.txt), including the precise variational formula, six sections of research and audit requirements, and four primary mathematical references.

Its title and opening mathematical request are:

> Research task: Prove the full Mezard–Parisi formula for the Viana–Bray model

> Establish the finite-connectivity Mezard–Parisi variational formula below, including the low-temperature regime and without any finite-RSB hypothesis on the limiting Gibbs measure.

This is the original research request, preceding the September 21 audit, integration, and exposition prompts. September 21 dates the integrated edition archived here, rather than the beginning of the research attempt. The prompt's requirements describe what was requested; they do not certify that the resulting manuscript satisfies every requirement.

## Comparison with OpenAI's proof

This comparison uses OpenAI's **36-page [full manuscript, *The Mézard–Parisi formula for diluted spin glasses*](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/The-Mezard-Parisi-formula-for-diluted-spin-glasses-September-23-2026/paper.pdf)**, dated September 23, 2026. OpenAI also released an abridged reasoning summary; the full manuscript is the reference here. Links below identify the version compared.

**Both manuscripts claim the same pressure formula on their shared Viana–Bray setting. OpenAI states a broader model theorem; the main arguments for the reverse inequality are substantially different.**

| Aspect | This 46-page manuscript | OpenAI's manuscript |
| --- | --- | --- |
| Interaction class | Two-spin Viana–Bray with bounded symmetric couplings | Even-arity interactions satisfying the Panchenko–Talagrand factorization and positivity hypotheses |
| Couplings and field | Bounded couplings and a fixed deterministic dimensionless field | First-moment integrability; independent identically distributed random fields are allowed |
| Named models | Viana–Bray | Viana–Bray, diluted even-spin models, and soft even-*K* SAT |
| Variational statement | Infimum over all finite cascade depths | Infimum over all finite hierarchy depths |
| Zero temperature | No separately stated corollary | Expected ground-state value as a limit of the positive-temperature variational values |

For scope, compare this manuscript's **Theorem 1.1 (p. 2)** with OpenAI's **Theorem 2.1 (p. 4)** and **Corollaries 10.1–10.3 (pp. 34–35)**; see its [model and hypotheses](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/The-Mezard-Parisi-formula-for-diluted-spin-glasses-September-23-2026/build/sections/model.tex) and [named-model consequences](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/The-Mezard-Parisi-formula-for-diluted-spin-glasses-September-23-2026/build/sections/consequences.tex). Neither formula requires attainment at a finite depth. OpenAI's zero-temperature corollary takes a temperature limit; it does not introduce a separate explicit zero-temperature order-parameter formula.

**Shared starting point.** Both use the interpolation upper bound and address the difficulty that pair overlaps alone do not determine the spin patterns needed by diluted cavity terms. Their task for the reverse inequality is to recover admissible hierarchical messages without losing the pressure.

**This manuscript's route: exact structure of a selected auxiliary law.** Section 3 selects a stationary minimizing spin law. Sections 4–6 enlarge its feature family using actual cluster centres, products, and iterated centres, together with Gaussian stationarity and marked Ghirlanda–Guerra identities. Theorem 7.1 (p. 38) claims exact conditional independence of site rows given the enriched master genealogy. Proposition 8.1 (pp. 42–44) then recovers the cavity value through finite cascade approximations. The structural statement concerns this specially selected auxiliary minimizer. Its master overlap contains enriched feature information; it is not a claim that the ordinary pair overlap determines every unperturbed physical Gibbs state.

**OpenAI's route: averaged control on finite auxiliary trees.** Bounded marked Poisson perturbations produce identities for prescribed replica trees. Shifting their internal branching depths controls the small coefficients in those identities. A conditional-covariance induction gives multioverlap concentration averaged over branching depths, enough to replace site labels by independent hierarchical messages in the cavity calculation. The limit in system size is taken at fixed hierarchy depth, followed by increasing depth. See **Sections 6–8**, especially **Theorem 7.1** and **Proposition 8.3**, and the [proof outline](https://github.com/openai/math/blob/adc7f1241b42e322a6451854ab7e4b4c146bf78a/preprints/The-Mezard-Parisi-formula-for-diluted-spin-glasses-September-23-2026/build/sections/overview.tex).

Thus this manuscript pursues an exact representation of an enriched auxiliary spin law, whereas OpenAI obtains the averaged finite-tree estimates needed for the pressure comparison. These structural outputs concern different auxiliary objects; they are not a simple stronger-versus-weaker theorem comparison.

**Trial notation.** This manuscript uses magnetizations and explicitly weighted cascades; OpenAI uses effective fields and successive power means. The message conversion is $u=\tanh x$; boundary magnetizations $u=\pm1$ correspond to limits $x\to\pm\infty$. Root randomness is another parametrization difference: this manuscript's Proposition 2.5 (pp. 9–10) explains how an extra level with exponent tending to zero absorbs independent site-root marks. Literal fixed-depth trial classes should not be identified without these adjustments.

**Chronology and review status.** The recovered integrated edition here is dated September 21; OpenAI's manuscript is dated September 23. These document dates alone establish neither first discovery nor public priority or independence. This comparison describes statements and proof mechanisms, not a new complete audit of either argument. The audit status of the archived manuscript remains as stated below.

## Audit record and limits

The favorable September 21 audit concerned the **59-page precursor**. It should not be treated as a separate end-to-end certification of this later PDF.

The October 6 Pacific / October 7 UTC review of the exact archived 46-page PDF examined source statements and hypotheses, including Sections 4–5 and Theorem 1.1. Its recorded conclusions were `mathematical_gap_demonstrated: false` and `full_formula_verified: false`. An older scope-audited draft also had 46 pages; it is a different file and its assessment must not be substituted for the assessment of this edition.

Complete verification still requires the structural constructions and their applications to be checked together, including marked Gaussian stationarity, canonical-centre compatibility and preservation, the marked identities and enrichment, the common hierarchy, conditional row independence, and finite-cascade recovery. Unfinished formalization of these steps is not itself a demonstrated mathematical gap. Existing component checks do not certify the full formula.

See [the audit-status summary](AUDIT-STATUS-2026-10-07.txt) for the precise boundary of the available assessment. This archive does not claim completed formal verification, external peer review, or a zero-error certificate.

## Files

- [viana_bray_integrated.pdf](viana_bray_integrated.pdf) — unchanged 46-page integrated manuscript.
- [AUDIT-STATUS-2026-10-07.txt](AUDIT-STATUS-2026-10-07.txt) — summary of existing review records, not a new whole-paper audit.
- [ORIGINAL-PROMPT.txt](ORIGINAL-PROMPT.txt) — the complete September 20 research brief, preserved verbatim.
- [PROVENANCE.json](PROVENANCE.json) — edition identity, chronology, original-prompt identity and audit boundaries.
- [SHA256SUMS.txt](SHA256SUMS.txt) — checksums for this package.

The manuscript contains its bibliography and attribution of mathematical inputs. Its inclusion here records AI-generated research and its review status; it does not establish independence from prior literature or certify novelty.
