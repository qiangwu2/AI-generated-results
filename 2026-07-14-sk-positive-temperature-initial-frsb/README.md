# Initial full-RSB interval for SK at positive temperature

**Initial development: July 14, 2026 (UTC).** This folder preserves the revised 34-page reference edition of an AI-generated mathematical argument developed in user-guided ChatGPT sessions, together with its October 6, 2026 recheck.

## Result

For the zero-field Sherrington–Kirkpatrick model, with normalization $\xi(q)=\beta^2q^2/2$, the manuscript establishes that for every finite inverse temperature $\beta>1$ there is $q_\beta>0$ such that

$$
[0,q_\beta]\subseteq\mathrm{supp}\,\mu_\beta.
$$

It also derives no atom at zero, $\beta u_{xx}(0,0)=1$, $u_{xxxx}(0,0)<0$, and a smooth Parisi distribution function on $[0,q_\beta)$. The scope is an **initial interval** in the support at positive temperature. The manuscript does not establish connectedness of the entire support or a zero-temperature theorem.

## When the argument was obtained

- **July 14, 2026 (UTC):** the initial interval argument was developed after studying Patrick Lopatto’s v1 on infinite support. The recovered conversation contains the initial proposal, an 18-page draft, and successive analytic revisions.
- **July 14 conversation, later revision:** the readable reference edition was produced from a 23-page revised core, with a 3-page reader’s guide and an 8-page Appendix R. This is the 34-page PDF preserved here, whose printed date is July 14, 2026. The recorded turn requesting this edition began at 23:53 UTC; turn timestamps do not establish the exact PDF completion time.
- **October 6, 2026 (Pacific time; October 7 UTC):** the historical materials were recovered and the 34-page edition was carefully rechecked. The PDF was subsequently downloaded and matched against the reviewed page captures. This repository package and README were prepared at that time; the historical PDF is preserved unchanged.

These dates document the development history. They are not a claim of an earlier public publication or a certification of priority over other work.

## Audit status

The fresh recheck found **no fatal mathematical error or unresolved substantive gap in the main initial-interval argument**. It covered the analytic estimates, slope-cone preservation and closure, strict first-gap inequality, marginality, absence of an atom at zero, and exclusion of small support gaps.

The historical PDF still needs four local corrections, documented in [the audit report](AUDIT-2026-10-06.txt):

1. Require positive curvature explicitly in the general slope-coordinate setup; strict convexity alone is insufficient.
2. Supply the weighted derivative estimate omitted from the inverse-function justification in Appendix A.
3. Restrict the finite-profile construction so that a decrease to parameter zero is the final operation.
4. Correct the endpoint wording in the citation of Auffinger–Chen’s smoothness theorem.

The audit explains why these repairs use assumptions or estimates already available and preserve the main conclusion. They have **not** been silently inserted into the archived PDF. This is an AI-assisted mathematical audit, not formal verification or external peer review, and it does not certify the file as literally error-free.

## Files

- [FRSB_initial_interval_readable_latest.pdf](FRSB_initial_interval_readable_latest.pdf) — the original 34-page readable reference edition, unchanged.
- [AUDIT-2026-10-06.txt](AUDIT-2026-10-06.txt) — the detailed recheck, including exact locations and repairs for the four local issues. Its description of browser captures records the evidence available when the audit was completed; the PDF binary was recovered afterward.
- [PROVENANCE.json](PROVENANCE.json) — edition identity, archive dates, and checksums.
- [SHA256SUMS.txt](SHA256SUMS.txt) — checksums for the archived files.

## Sources and attribution

The argument builds on Patrick Lopatto’s finite-profile slope-coordinate method in [arXiv:2607.11756v1](https://arxiv.org/abs/2607.11756v1). It is not independent of that input. The principal analytic and variational inputs are [Auffinger–Chen, *On properties of Parisi measures*](https://arxiv.org/abs/1303.3573) and [Jagannath–Tobasco, *Some properties of the phase diagram for mixed p-spin glasses*](https://arxiv.org/abs/1504.02731).

The manuscript’s extension passes the slope inequalities to arbitrary profiles and combines a direct strict first-gap argument with near-origin rigidity to obtain the initial support interval. This description records the argument’s relationship to its cited inputs; it is not a separate novelty or priority certification.
