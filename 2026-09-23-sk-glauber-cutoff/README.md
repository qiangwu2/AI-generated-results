# Cutoff for SK Glauber dynamics at fixed inverse temperature below 1/3

**Developed September 23, 2026 (Pacific time).** This folder preserves the 10-page proof manuscript and the original research prompt from the Codex chat **“Prove SK Glauber cutoff.”** The completed proof and revised PDF were delivered on September 24 in UTC; the manuscript and folder use the local September 23 date.

[Read the manuscript](sk_cutoff_proof.pdf) · [Original prompt](ORIGINAL-PROMPT.txt)

## Human contribution and AI generation

The proofs in this repository were generated almost entirely by AI. My role was primarily to prompt the models and request further work, audits, and revisions. I barely contributed any mathematical insights, proof ideas, or proof strategies.

I take neither credit nor responsibility for these results, as I have not had time to carefully check the proofs myself.

The results have undergone several rounds of AI auditing and revision. Within the scope of those reviews, no obvious unresolved substantive errors or gaps were identified. Known local corrections and checks that remain incomplete are summarized in each result's README.

Due to limited computational resources, we have only been able to verify parts of them in Lean. Where provided, this verification covers the formalized statements and is conditional on explicitly stated assumptions. These checks do not guarantee that the complete proofs are correct or free of gaps. Please use the results with caution.

## Result and scope

The manuscript establishes quenched, worst-case total-variation cutoff for the **zero-field Sherrington–Kirkpatrick model**, for every fixed $0<\beta<1/3$, in continuous time with **rate one per site**. The couplings are symmetric, with zero diagonal and independent $J_{ij}\sim\mathcal N(0,1/N)$ for $i<j$. The maximum over starting configurations is taken after fixing the disorder, so the statement includes disorder-dependent starting states.

For every fixed $0<\varepsilon<1/2$,

$$
\frac{t_{\mathrm{mix}}^{N,J}(\varepsilon)}{t_{\mathrm{mix}}^{N,J}(1-\varepsilon)}
\xrightarrow[N\to\infty]{\mathbb P_J}1.
$$

Writing $a_\beta=1-2\beta-3\beta^2>0$, the manuscript gives, on disorder events of probability tending to one,

$$
t_{\mathrm{mix}}^{N,J}(\varepsilon)-t_{\mathrm{mix}}^{N,J}(1-\varepsilon)
\le \frac{6}{a_\beta}\log\frac1\varepsilon,
$$

and

$$
t_{\mathrm{mix}}^{N,J}(1-\varepsilon)
\ge \frac12\log N-\frac12\log\frac{16}{a_\beta\varepsilon}.
$$

The mixing time is also of order $\log N$ for fixed accuracy, using the cited upper bound of Wang. The bounded window is a bound between mixing-time quantiles. The proof does **not** identify the leading positive-temperature constant, a deterministic center accurate to order one, or a limiting profile. It does not include $\beta=1/3$, the whole interval $\beta<1/2$, or external fields in the cutoff theorem. The appendix separately checks the independent-spin benchmark at $\beta=0$.

## Proof idea

The key estimate propagates a Poincaré inequality for the **evolving probability law** $\nu_t=\nu_0P_t$, starting from any product law, including a point mass. The proof differentiates that law's own optimal heat-bath Poincaré constant, retains the signs of the interaction matrix, and absorbs the remaining interaction term into a negative square. It does not assume that the evolving law is an Ising measure.

For $B=\beta J$, set $M=\max_{i,j}|B_{ij}|$ and $R=\max_i\sum_jB_{ij}^2$. The deterministic condition is

$$
k=\|B\|_{\mathrm{op}}+(2e^{4M}+e^{8M})R<1.
$$

The resulting Poincaré bound gives a local inequality for the original generator. A moving-reference chi-square contraction and overlap argument then gives the bounded mixing window. A linear test statistic and spectral Jensen inequality give the logarithmic lower bound. For SK, $k\le2\beta+3\beta^2+o(1)$ with high probability, yielding the range $\beta<1/3$.

The local-product argument is attributed to [Pedrotti–Salez, version 1](https://arxiv.org/abs/2607.05345v1), with its needed finite-state calculations included in the PDF. The matrix estimates and additional logarithmic upper-order mixing bound are attributed to [Wang, version 2](https://arxiv.org/abs/2608.22159v2). These dependencies are recorded explicitly; this archive makes no blanket claim of independence from prior literature or of research priority.

## Original research prompt

The [full original prompt](ORIGINAL-PROMPT.txt) is preserved byte for byte from the user-supplied attachment: 13,546 bytes, SHA-256 `794756e5942e6993631443807591209105a8ff19a2581869e3d1338dec7fe32e`.

It was a detailed research specification, beginning:

> Research prompt: Cutoff for Glauber dynamics of the SK model
>
> This prompt adapts the precise task specification, independent proof search, and critical verification structure of the OpenAI Cycle Double Cover prompt.

It specified the model and clock, quenched worst-case quantifiers, a primary target $0<\beta<1/4$, a preferred extension to $\beta<1/2$, possible proof mechanisms, and explicit checks for disorder dependence, signed interactions, large local fields, and accumulated errors. An explicit cutoff location and a wider temperature interval were optional refinements. The claimed final range $0<\beta<1/3$ exceeds the primary target but does not reach the preferred extension.

## How the proof was generated

This was **almost entirely AI-generated proof development, with human prompting and repeated AI audits**. The user supplied the detailed prompt, pressed for a proof after partial results, and requested a fresh audit and PDF. The AI developed and wrote the argument, using parallel agents for separate approaches and critical checks. The recovered record does not establish a verified model/version label, so none is assigned here.

The recorded work rounds were:

| September 23, 2026, Pacific time | Recorded outcome |
|---|---|
| 15:31:31–16:11:26 | Initial prompt and first attempt: independent-spin/vanishing-inverse-temperature comparison and a precise unresolved evolving-law inequality; no fixed-positive-temperature cutoff proof. |
| 16:23:21–16:57:49 | Further approaches: a fixed-temperature variance estimate and mixing lower bound; still no cutoff proof. |
| 17:15:28–18:09:17 | After the user requested continued work, the evolving-law Poincaré argument produced the claimed cutoff theorem for every fixed $0<\beta<1/3$, with three agent audits reported. |
| 18:56:43–19:12:05 | At the user's request, a fresh main-agent and three-reviewer audit expanded the multiplicity and singular-initial-law arguments, supplied a direct finite-state contraction proof, and delivered the revised 10-page PDF. |

These are recorded turn start/completion times, not exact timestamps for individual insights or file writes. The earlier incomplete research notes are superseded by the final manuscript for the theorem archived here. The complete sequence took several work rounds and revisions; calling the final proof “one-shot” would be inaccurate.

## Audit status

The contemporaneous September 23 audit records **no remaining mathematical gap found in the revised proof on the stated range**. It describes a main-agent review, three agent reviewers with different assignments, and a review of the LaTeX transcription. The checked points include the exact evolution identity, global derivative estimates, square completion, repeated eigenvalues, singular starts, moving-reference chi-square contraction, worst-case quantifiers, disorder estimates, and clock normalization.

Two finite-state implementations tested the identity and bounds on arbitrary laws and evolved endpoint laws; the report records 400 identity tests in one implementation and 500 arbitrary-law plus 300 evolved-law tests in the other, with no tested estimate failing.

This is a record of mathematical audits by AI agents, **not a guarantee of zero errors, independent human peer review, or a Lean formalization**. Finite-state numerical checks support the algebraic review but do not prove the asymptotic theorem. The repository preserves the existing manuscript; this summary is not a new full mathematical audit.

## Files

- `sk_cutoff_proof.pdf` — original revised 10-page manuscript, unchanged.
- `ORIGINAL-PROMPT.txt` — original user-supplied research prompt, unchanged.

Archived in this repository on October 6, 2026 (Pacific time; October 7 UTC).
