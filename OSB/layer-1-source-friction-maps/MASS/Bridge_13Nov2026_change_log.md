# Change log: MASS Regulatory Bridge, 13 Nov 2026 paper (corrected 14 Nov 2026)

Prepared 15 Nov 2026. Same-collaborator production: development evidence, not independent corroboration.

## Changes and drivers

| # | Where | Change | Driver |
|---|---|---|---|
| 1 | Exec summary 3; §6 | MSC 107 wording qualified ("at this stage") | Corrections A3 [P] |
| 2 | Exec summary 4; §3.2 Rule 17; §4.2 item 3 | Para 61 only; "observational/predictive" labelled the paper's own | A1 |
| 3 | §4.2 items 2 and 5; §4.3 | Paras 98(vi), 98(vii) added | A2 |
| 4 | §4.2 intro; §7.1 | Ever Smart verification scope: paras 1–118 read | A6 |
| 5 | §6 | Roadmap and 2036 remark added, flagged unverified | A5 [P] |
| 6 | §4.1 | "In sight" paragraph | B1 |
| 7 | §4.4; Appendix A | Lateral miss, dwell, course filter, degraded values, 17(a)/(b) values | B2–B6 |
| 8 | §4.4 | Degraded-state behaviour and simulation statement | B5, B7 |
| 9 | §7.1 | Adoption row: re-issue note [P]; simulation row; roadmap row; MSC 107 row | Corrections A3, A4; V-13 run |
| 10 | Appendix A | Station-keeping row: simulation limit stated | V-13 run |
| 11 | §4.4 | Seed-sensitivity sentence | V-13 run |

## Not adopted

Corrections A4 asked to soften the adoption date to "13–22 May". Kept **21 May 2026**: the IMO resolution text records it. §7.1 notes that some summaries say 22 May.

## Editorial additions not in the corrections file

§5.2 row "In sight and fusion" (from B1); cross-reference to item 5 in §4.2 item 2; revision line in the header.

## V-13 result (demo run, headless, 15 Nov 2026)

All five scenarios pass on the demo's fixed seeds. 40 other seeds: 199 of 200 passes; failure = scenario 2, seed 24, never left CROSSING. Degraded-state withholding of Rule 17 action: scenario 5 collides (closest approach 0.027 nm). Demo parameter panel now matches Appendix A except station-keeping (see #10). Fixed-seed results are identical before and after the HTML edit.

## Lineage (UAIRF §26.6)

Method: SHA-256 of both HTML files plus a line diff (17 changed lines); itemised list above for the paper. Limits: the paper has no hash of the 13 Nov PDF (rebuilt from extracted text, not byte-compared); no independent review.

| File | SHA-256 |
|---|---|
| rule_switching_demo.html (before) | b4412ecb5cf56153532caa53a4860cdeead24376c14ee47fadc6b86d12370be9 |
| rule_switching_demo.html (after) | 22120a837a2801ee1251c12b375223363b64b0e4547de721ce3899843b8a2188 |
