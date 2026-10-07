# Initial full-RSB interval for SK at positive temperature

**Initial development: July 14, 2026 (UTC).** This folder preserves the revised 34-page reference edition of an AI-generated mathematical argument developed through prompts to AI models in ChatGPT sessions, together with its October 6, 2026 recheck.

## Human contribution and AI generation

The proofs in this repository were generated almost entirely by AI. My role was primarily to prompt the models and request further work, audits, and revisions. I barely contributed any mathematical insights, proof ideas, or proof strategies.

I take neither credit nor responsibility for these results, as I have not had time to carefully check the proofs myself.

The results have undergone several rounds of AI auditing and revision. Within the scope of those reviews, no obvious unresolved substantive errors or gaps were identified. Known local corrections and checks that remain incomplete are summarized in each result's README.

Due to limited computational resources, we have only been able to verify parts of them in Lean. Where provided, this verification covers the formalized statements and is conditional on explicitly stated assumptions. These checks do not guarantee that the complete proofs are correct or free of gaps. Please use the results with caution.

## Result

For the zero-field Sherrington–Kirkpatrick model, with normalization $\xi(q)=\beta^2q^2/2$, the manuscript establishes that for every finite inverse temperature $\beta>1$ there is $q_\beta>0$ such that

$$
[0,q_\beta]\subseteq\mathrm{supp}(\mu_\beta).
$$

It also derives no atom at zero, $\beta u_{xx}(0,0)=1$, $u_{xxxx}(0,0)<0$, and a smooth Parisi distribution function on $[0,q_\beta)$. The scope is an **initial interval** in the support at positive temperature. The manuscript does not establish connectedness of the entire support or a zero-temperature theorem.

## When the argument was obtained

- **July 14, 2026 (UTC):** the initial interval argument was developed after studying Patrick Lopatto’s v1 on infinite support. The recovered conversation contains the initial proposal, an 18-page draft, and successive analytic revisions.
- **July 14 conversation, later revision:** the readable reference edition was produced from a 23-page revised core, with a 3-page reader’s guide and an 8-page Appendix R. This is the 34-page PDF preserved here, whose printed date is July 14, 2026. The recorded turn requesting this edition began at 23:53 UTC; turn timestamps do not establish the exact PDF completion time.
- **October 6, 2026 (Pacific time; October 7 UTC):** the historical materials were recovered and the 34-page edition was carefully rechecked. The PDF was subsequently downloaded and matched against the reviewed page captures. This repository package and README were prepared at that time; the historical PDF is preserved unchanged.

These dates document the development history. They are not a claim of an earlier public publication or a certification of priority over other work.

## How the proof was generated

**An initial strategy proposed in one response, followed by iterative auditing and substantive revision.** The recovered chats show that the user first supplied Lopatto's v1 and requested an audit, then asked whether its infinite-support result could be strengthened to interval support. The next assistant response proposed the initial-interval theorem and its main proof strategy. That response explicitly acknowledged that arbitrary-profile closure and endpoint estimates still needed a complete analytic write-up.

The visible production sequence was:

| Recorded turn on July 14, 2026 (UTC) | Output and role |
| --- | --- |
| 06:13 | Reading and audit of Lopatto's v1. |
| 06:43 | Initial-interval proposal and conceptual proof strategy, in one response to the improvement request. |
| 07:18 | First 18-page manuscript. |
| 16:30 | Revised manuscript correcting a logarithmic-weight sign and expanding endpoint estimates and slope-cone preservation. |
| 18:45 | Revised 23-page manuscript repairing the weighted half-line argument, approximation/Itô passage, and endpoint estimates. |
| 22:06 | Further repaired 23-page core, including a direct general-profile remainder argument and higher derivative bookkeeping. |
| 23:53 | Readable 34-page edition: a 3-page guide, the unchanged repaired 23-page core, and an 8-page Appendix R. |

Thus the main recorded chain contains **one proposal response and five PDF-production/revision responses**, following the initial v1 audit, with additional audit exchanges between them. The three substantive revision rounds repaired mathematical details; the last production round assembled the readable edition. The archived manuscript is therefore not a one-shot finished proof. “Several rounds of generation, audit, and revision” describes the process more precisely than “few-shot.” These are visible conversation turns, not a count of underlying model calls; their timestamps do not establish exact response or PDF completion times.

The user's prompting included supplying the starting paper, requesting the strengthening target and rigorous checking, relaying AI audit feedback, and requesting revisions and clearer exposition. AI assistants proposed the mathematical strategy, developed and checked the argument, and generated the manuscripts. This was **almost entirely AI-generated proof development, with human prompting**, followed by repeated AI audits and corrections.

## Comparison with Lopatto's v2 and v3

The main initial-interval conclusion here has the same scope as [Lopatto's v2, Theorem 1.1](https://arxiv.org/html/2607.11756v2): for every finite inverse temperature greater than one, the zero-field SK Parisi support contains an interval beginning at zero. [V3, Theorem 1.1](https://arxiv.org/html/2607.11756v3) is stronger: the entire support is one interval, with a smooth density below its upper endpoint and a positive atom at that endpoint. This manuscript does not establish that global conclusion.

The proof strategy is closely related to v2, with a distinct route through one essential lemma:

| Step | This manuscript and v2 |
| --- | --- |
| Arbitrary-profile extension | Both extend the finite-profile slope inequalities inherited from v1 by approximation and endpoint control. |
| Accumulation at zero | Both use a strict first-gap crossing argument and Parisi optimality, then obtain marginality and absence of an atom at zero. |
| Strict fourth derivative at the origin | This manuscript closes the slope inequalities down to parameter zero and uses their monotonicity to prove $u_{xxxx}(0,0)<0$. V2 proves the same sign through a separate killed-diffusion/Feynman–Kac argument and reflection-principle estimate. |
| Exclusion of small support gaps | Both obtain positivity of the third derivative of the self-consistency function on sufficiently small gaps. This manuscript uses strict Hermite–Hadamard; v2 uses a positive weighted integral identity. These express the same convexity contradiction with the endpoint optimality conditions. |

See this manuscript's Proposition 4.2 and near-origin argument, and [v2, §§3–7](https://arxiv.org/html/2607.11756v2), especially Lemma 6.3 and Lemma 7.3. The difference in the strict fourth-derivative argument is substantive; the final convexity step is an equivalent presentation of the same mechanism.

The initial argument is recorded on July 14, while v2 and v3 were submitted on July 15 and July 16, respectively, according to the [arXiv submission history](https://arxiv.org/abs/2607.11756). The work explicitly builds on v1, submitted July 13. This chronology documents the recovered development history and does not by itself establish priority or historical independence.

## Audit status

The fresh recheck found **no fatal mathematical error or unresolved substantive gap in the main initial-interval argument**. It covered the analytic estimates, slope-cone preservation and closure, strict first-gap inequality, marginality, absence of an atom at zero, and exclusion of small support gaps.

The historical PDF still needs four local corrections:

1. Require positive curvature explicitly in the general slope-coordinate setup; strict convexity alone is insufficient.
2. Supply the weighted derivative estimate omitted from the inverse-function justification in Appendix A.
3. Restrict the finite-profile construction so that a decrease to parameter zero is the final operation.
4. Correct the endpoint wording in the citation of Auffinger–Chen’s smoothness theorem.

The audit found that these repairs use assumptions or estimates already available and preserve the main conclusion. They have **not** been silently inserted into the archived PDF. This is an AI-assisted mathematical audit, not formal verification or external peer review, and it does not certify the file as literally error-free.

## Files

- [FRSB_initial_interval_readable_latest.pdf](FRSB_initial_interval_readable_latest.pdf) — the original 34-page readable reference edition, unchanged.

## Sources and attribution

The argument builds on Patrick Lopatto’s finite-profile slope-coordinate method in [arXiv:2607.11756v1](https://arxiv.org/abs/2607.11756v1). It is not independent of that input. The principal analytic and variational inputs are [Auffinger–Chen, *On properties of Parisi measures*](https://arxiv.org/abs/1303.3573) and [Jagannath–Tobasco, *Some properties of the phase diagram for mixed p-spin glasses*](https://arxiv.org/abs/1504.02731).

The manuscript’s extension passes the slope inequalities to arbitrary profiles and combines a direct strict first-gap argument with near-origin rigidity to obtain the initial support interval. This description records the argument’s relationship to its cited inputs; it is not a separate novelty or priority certification.
