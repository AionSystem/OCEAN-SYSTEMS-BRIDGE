# IAAP v0.2.1 — Institutional Alignment & Adoption Protocol

**Companion negotiation and strategic adoption layer for UCFS v0.3 and ARCVB**

| Field | Value |
|---|---|
| Document | IAAP v0.2.1 — Institutional Alignment & Adoption Protocol |
| Supersedes | IAAP v0.2 (and v0.1) |
| Revision type | Defect correction and [P] evidence update. Not a substantive revision under UCFS v0.3 §28.5 (see §7.1.4). |
| Role | Strategic adoption, institutional alignment, stakeholder negotiation and interface specification |
| Parent stack | UCFS v0.3 (normative spec) → ARCVB (execution pipeline) → MASS Regulatory Bridge (13 Nov 2026 source map) |
| UCFS version dependency | v0.3. IAAP v0.1 was written against UCFS v0.2; the clauses it referenced have been superseded in v0.3. This version re-references every UCFS clause to v0.3 and flags each dependency in §6. |
| Status | Working draft. Not a standard. Not a substitute for legal or regulatory advice. Not an assurance that any institution will adopt UCFS or ARCVB. |
| Provenance | Same-collaborator production with UCFS v0.2, UCFS v0.3 and the UAIRF v1.1 review. Development evidence, not independent corroboration. |
| Evidence base | Annex E (retrieved 14 Nov 2026 from secondary sources and search summaries; every item is [P] until checked against the primary text). |
| Conventions | MUST, MUST NOT, SHOULD, SHOULD NOT, MAY in the RFC 2119 sense. The [P] flag is used as defined in UCFS v0.3 §2.2. |

> **Notice.** IAAP describes how the UCFS/ARCVB stack may be presented, sequenced and negotiated with institutions. It does not assert that any institution will accept it, does not substitute for Administration approval, and does not modify any UCFS clause. Where IAAP and UCFS disagree, UCFS governs. IAAP is not legal advice; institutional-engagement strategies should be discussed with counsel and with the institution's own process owners before deployment.

---

## §0 — Changes from v0.1

### 0.1 Version alignment (critical)

**0.1.1** IAAP v0.1 was written against UCFS v0.2. The UCFS line has since advanced to v0.3, produced after a full UAIRF v1.1 adversarial review of v0.2. IAAP v0.2 is re-referenced to UCFS v0.3.

**0.1.2** The following UCFS v0.2 clauses that IAAP v0.1 relied on have been materially changed in v0.3, and IAAP v0.2 references the v0.3 form:

| Clause | v0.2 form | v0.3 form |
|---|---|---|
| §5.4 (non-waivable list) | Residues and bounded claims both treated as S1 in non-waivable domains | Residues S1; bounded claims S2 with runtime escalation (§5.4.2, §8.10.3) |
| §4.2 (conformance vector) | Vector was conformance | Vector is measurement; conformance is a separate gate-based claim (§4.1.1–4.1.3) |
| §5.2 (gates) | G2 did not require runtime monitor evidence; G6 did not require V&V results | G2 requires runtime monitor evidence (§5.2.4); G6 requires V&V results (§5.2.5) |
| §26.8 (disclosure) | "Counsel sign-off" was vague | §26.8.3 defines a testable criterion |
| §28.5 (stability) | Absolute annual cadence | Defect-correction exception; single-cycle declaration for v0.1→v0.2→v0.3 (§28.5.1, §28.5.2) |
| §28.6 (conformance mark) | Active | Suspended until Annex I is populated (§28.6.1) |
| §24.4 (runtime bridge) | Asserted as established | Downgraded to [P] proposed claim (§24.4.1) |

**0.1.3** IAAP v0.2 introduces the following sections that v0.1 did not have, and that the stack's own discipline requires:

- §1.5 Limits — what IAAP is not.
- §2.3 [P] discipline — counterparty fears are inferences, not facts.
- §4 Gate-to-rule mapping — every pre-engagement gate maps to one of the four architectural rules.
- §5 Failure paths — what to do when an institution refuses.
- §6 Stack integration — every UCFS v0.3 clause IAAP depends on, with its current form.
- §7 Governance and stability.
- Annex A — [P] register.
- Annex B — Open items.
- Annex C — Lineage declaration.
- Annex D — Resolution log.
- Annex E — Evidence base (added in v0.2.1).

### 0.2 Renamings (framing fixes)

**0.2.1** "Gatekeeper-bypass specification" is removed. The role line now reads "Strategic adoption, institutional alignment, stakeholder negotiation and interface specification." The word *bypass* signalled an intent to route around institutions, which contradicts Rule 1 (Asymmetric Empathy) and Rule 3 (Unimpeachable Provenance). The framework must not do to itself what it is designed to prevent.

**0.2.2** "Trojan Horse Diagnostic" is renamed "Zero-Threat Diagnostic." The Trojan Horse is the canonical bluff-and-conquer myth; naming a phase after it will be read as hostile by any technical counterparty. The zero-threat framing says what the phase is actually for: enter the institution without triggering the "not invented here" immune response.

**0.2.3** Phase 4's "inescapable industry standard" and "every new user adds gravity to your ecosystem" are removed. Those phrases are the "viral" framing that Gate I-1 (v0.1) already told the reader to remove. The stability commitment (UCFS v0.3 §28.5) is the correct expression of the same goal: the schema does not shift unpredictably. That is what Phase 4 actually delivers.

**0.2.4** "Gatekeeper" is retained only where the reader understands it as the institution whose decision the adopter needs. Where the reference is to a specific institution, the term used is "counterparty" (neutral) or "co-regulator" (for flag-State administrations) or "co-standards-setter" (for classification societies). The word *gatekeeper* in v0.1 carried an outsider posture that will cost adoption.

**0.2.5** "Surrender the High Ground" is renamed "Declare the Limits Honestly." The move itself (open with what the system cannot do) is right. The v0.1 framing as a negotiating technique — "why it works: every vendor over-promises" — will be seen through by a sophisticated co-regulator and will discount the declaration. v0.2 reframes: the limits are declared because they are real, not because declaring them is a tactic.

### 0.3 Fixes carried into v0.2

**0.3.1** The pre-engagement checklist's numbering gap (v0.1 had items 1, 2, 3, 7, 9 instead of 1–5) is corrected to a clean I-1 through I-5.

**0.3.2** The five pre-engagement gates are mapped to the four architectural rules in §4.1.

**0.3.3** Phase 3 ("Legitimacy Win") now carries a real-win guard: the win must reduce the counterparty's actual exposure, not merely appear to (§3.3.3).

**0.3.4** A failure-path section is added (§5), covering rejection, competitive-treatment of UCFS by a class society, and regulator non-recognition across ports.

**0.3.5** Each counterparty fear in §2 is tagged [P] and listed in Annex A, with the validation route.

**0.3.6** A provenance/limits section (§1.5) is added.

**0.3.7** A stability/governance section (§7) is added, aligned to UCFS v0.3 §28.5 and §28.5.2.

### 0.4 Not adopted from the review

**0.4.1** A full UAIRF v1.1 review of IAAP is not performed here. The prior review of UCFS v0.2 surfaced systemic issues (schema reconciliation, self-application, lineage) that would require a full adversarial pass to work through. IAAP v0.2 records the recommendation in Annex B, item B-9.

### 0.5 Changes from v0.2 (this version, v0.2.1)

**0.5.1** v0.2.1 is a defect correction and [P] evidence update. It adds no new rules, phases or gates, and is not a substantive revision under UCFS v0.3 §28.5. Where the body text still says "IAAP v0.2", it means the v0.2 baseline text carried forward into v0.2.1.

**0.5.2** Evidence corrections (sourced in Annex E, all [P]):

- §1.4.3 corrected: the IMO MASS Code is non-mandatory (adopted 22 May 2026, effective 1 July 2026); approval remains national.
- §1.2.4, §3.4 and new §7.5 carry the dated IMO timeline (experience-building phase 2026–28; mandatory code targeted for 1 January 2032 at the earliest).
- §2.2.1, §3.1 and §3.3 name the current US instruments: USCG Work Instruction 5P-WI-002(1) and 46 C.F.R. § 15.715.
- §2.2.2 and A-3/A-4 revised: class societies are launching their own autonomy notations (e.g., DNV AROS), so the fear is parallel-framework fragmentation rather than displacement. B-3 now names AROS as the first mapping task.
- §2.2.3 and A-5/A-6 revised: the GAO Navy autonomy finding concerns organisational fragmentation and early requirement lock-in, not crew-check conversion. The IMO MASS Code excludes warships.
- A-12 and §2.2.4 carry citations (*Ever Smart*; *The Pennsylvania* tagged [P]).

**0.5.3** Framing and structure corrections:

- §3.1.3 and Gate I-3: authorship and framework lineage MUST be disclosed on request and in anything the counterparty circulates onward (Rule 3).
- Gate I-2 reworded from individual career protection to institutional exposure and a defensible administrative record.
- B-9 and §7.3.2: an external practitioner review is added alongside the UAIRF self-pass.
- §3 paragraphs are numbered (this fixes the dangling §3.3.4 reference); §0.1.3 now lists Annex D; the unsupported "ten minutes" figure in §3.2 is removed.
- B-11 added: tension between the annual cadence and the experience-building phase feedback loop. B-12 added: primary-text verification of Annex E.

---

## §1 — Purpose, Philosophy and Limits

### 1.1 Purpose

**1.1.1** IAAP is the fourth layer of the UCFS stack. UCFS structures regulatory uncertainty into claims; ARCVB executes the claims at runtime; the MASS Regulatory Bridge maps the legal friction. IAAP governs how the stack is presented, sequenced and negotiated across the institutions whose decisions the adopter needs.

**1.1.2** IAAP applies to four classes of counterparty: flag-State administrations (co-regulators), classification societies (co-standards-setters), defense acquisition and prime contractors, and maritime counsel and insurers. It also applies, with adjustments, to commercial autonomy developers as adopters rather than counterparties.

**1.1.3** IAAP does not itself produce technical content. It produces engagement strategy, interface documents, and negotiation protocols that make the technical content usable.

### 1.2 Architectural philosophy (retained from v0.1)

**1.2.1 Rule 1 — Asymmetric Empathy.** Every counterparty has a primary institutional fear: personal liability, career risk, statutory violation, or public failure. Never ask an institution to absorb unquantified risk. Engineer the deliverable so that adopting the stack reduces the counterparty's exposure relative to the status quo.

**1.2.2 Rule 2 — The "Would It Help?" Filter.** Treat bureaucratic friction, legal pushback and institutional skepticism as input telemetry, not personal rejection. Discard ego-driven arguments. Retain only artifacts that move the counterparty toward a verifiable decision gate.

**1.2.3 Rule 3 — Unimpeachable Provenance.** Never bluff, over-claim, or upgrade the verification status of a source. Institutional trust is built by voluntarily flagging the stack's own limits, provisional assumptions [P], and open residues before the auditor finds them. This rule is the framework's own ethical spine; without it, IAAP becomes a manipulation manual and violates its own stated purpose.

**1.2.4 Rule 4 — Temporal Asymmetry.** Commercial software iterates in days. International maritime treaties and defense procurement cycles move in years. Design modular, version-locked interfaces that endure long institutional wait times without requiring architectural rewrites. The IMO timeline is now concrete ([P], §7.5): an experience-building phase runs 2026–28 and a mandatory code is targeted for entry into force on 1 January 2032 at the earliest.

### 1.3 What IAAP is

**1.3.1** IAAP is a protocol for moving a technical framework into institutional practice. It specifies phases, gates, counterparty mappings, and interface documents.

**1.3.2** IAAP is adopter-agnostic. It does not assume the adopter is the architect of UCFS. It assumes the adopter is a person or team who has the UCFS/ARCVB stack and needs an institution to accept some part of it.

**1.3.3** IAAP is counterparty-specific. It assumes different institutions need different things from the same stack. The counterparty matrix (§2) is the operative artifact.

### 1.4 What IAAP is not

**1.4.1** IAAP is not a substitution for real piloting. The phases are designed to culminate in a genuine operational engagement; the diagnostic, the honesty, the legitimacy win, and the standardization are all scaffolding around an actual pilot. An adopter who runs all four phases without a pilot has produced a negotiation, not an adoption.

**1.4.2** IAAP is not a negotiation substitute for legal counsel. Institutional engagement strategies involve statutory, contractual and liability questions. Counsel must be consulted before any engagement that touches any of these.

**1.4.3** IAAP is not a substitute for Administration approval. No phase of IAAP substitutes for the approval process under national law. The IMO MASS Code is non-mandatory (effective 1 July 2026) and creates no binding approval route. No adoption event under IAAP creates a legal obligation on any Administration.

**1.4.4** IAAP does not assert that the counterparty fears in §2 are correct. They are inferences from published pain points, tagged [P] in Annex A. Each must be validated per institution before the corresponding phase is deployed.

**1.4.5** IAAP does not assert that the UCFS/ARCVB stack is complete, correct, or independently validated. UCFS v0.3 is a working baseline; the review that produced it is a same-collaborator review, not independent corroboration.

**1.4.6** IAAP does not solve statutory complement, class-notation competition, or regulator non-recognition across ports. Those are structural problems. IAAP's four rules and four phases are the correct starting point; they are not the whole answer, and the open items in Annex B name where they are not.

### 1.5 Limits and provenance

**1.5.1** IAAP v0.2 is produced by the same collaborator that produced UCFS v0.2, UCFS v0.3, the Red Team Report on v0.1, and the UAIRF v1.1 review of v0.2. It is development evidence, not independent corroboration.

**1.5.2** The counterparty-fear matrix in §2 is a hypothesis, inferred from the MASS Regulatory Bridge, the GAO reports, the published positions of the named institutions, and the 14 Nov 2026 evidence base in Annex E. It is not a survey of institutional positions. Each cell is tagged [P] and listed in Annex A.

**1.5.3** The four-phase playbook in §3 is a proposed protocol, not a tested one. No institution has been engaged via this protocol in a documented way. Adoption results would be evidence; the protocol itself is not.

**1.5.4** The five pre-engagement gates in §4 are self-audit checks, not institutional certifications. Passing them does not make an engagement safe; failing them makes an engagement unsafe by IAAP's own standards.

**1.5.5** IAAP does not claim any institutional endorsement, adoption, or recognition of UCFS, ARCVB, IAAP, or the MASS Regulatory Bridge. None has been reported.

**1.5.6** Annex E was assembled from secondary sources and search summaries on 14 Nov 2026. Primary texts (the MASS Code articles, the USCG Work Instruction, the GAO report body) were not read in full. Each item is [P] until verified (Annex B, B-12).

---

## §2 — Counterparty Incentive & Friction Matrix

### 2.1 Purpose and discipline

**2.1.1** Before presenting UCFS v0.3 or ARCVB to any institution, map the counterparty to its primary institutional fear and deploy the corresponding architectural wedge.

**2.1.2** Each counterparty cell in §2.2 carries:

- the **primary institutional fear** — tagged [P] as a hypothesis;
- **what the counterparty actually needs** — tagged [P] as a hypothesis;
- the **architectural wedge** — a specific UCFS v0.3 clause or ARCVB component that is designed to meet the need;
- a **wedge limit** — what the wedge does not do, and what remains open.

**2.1.3** Counterparty fears are inferences from published pain points. They MUST be validated per institution before Phase 1 is deployed. Validation is a Phase 1 activity, not an assumption.

### 2.2 Matrix

#### 2.2.1 Flag-State administrations (e.g., US Coast Guard, UK Maritime and Coastguard Agency)

| Field | Value |
|---|---|
| Primary institutional fear | [P] Approving a novel system that causes a casualty; violating domestic statutes (e.g., 46 U.S.C. §§ 8301, 8101, 8502); creating inconsistent port-to-port rulings |
| What they actually need | [P] A repeatable, defensible administrative record that shows they did not waive statutory duties illegally; a route to approve without absorbing novel liability; consistency across ports |
| Architectural wedge | UCFS v0.3 §5.4 (NW-1 to NW-8) and §4.2 (conformance vector). The non-waivable list enforces minimums stricter than the flag State may itself impose — protecting the statutory boundary. The conformance vector measures what a submitter actually has, so the Administration is not the sole evaluator of its own approval. |
| Wedge limit | The non-waivable list is fixed in UCFS and the Administration MAY add to it (§5.4.1). It is not an approval; it is a claim-and-evidence structure that the Administration must still evaluate. Statutory complement (NW-3) cannot be waived by UCFS or by the Administration; the wedge shows the legal route, not a substitute for it. |
| Current US instruments [P] | USCG Work Instruction 5P-WI-002(1), *Oversight of Unmanned, Autonomous and Remote-Control Operations*, which cancels CVC Policy Letter 22-01 (Change 1): the OCMI keeps final authority, manning may not fall below 46 U.S.C. § 8301 and 46 C.F.R. Part 15, and the COLREG lookout duty is restated. 46 C.F.R. § 15.715: acceptance of crew-replacing automation rests on system capability, demonstrated continuing reliability and a planned maintenance regime. Verify against primary text (Annex E). |

#### 2.2.2 Classification societies (e.g., DNV, ABS, Lloyd's Register)

| Field | Value |
|---|---|
| Primary institutional fear | [P] A parallel assurance framework fragmenting approvals or undermining their notations. (As of Nov 2026 class societies are launching their own autonomy notations, e.g., DNV AROS, so overlap is more likely than displacement. Annex E.) |
| What they actually need | [P] A way to verify autonomous software and runtime edge cases without rebuilding their rulebooks from scratch; the ability to preserve their notation as the authoritative technical standard |
| Architectural wedge | UCFS v0.3 §1.8 (complementarity). UCFS is explicitly a claim-and-evidence layer, not a rule set. §1.8.4 states that where a class notation is more specific than a UCFS clause, the notation governs the technical requirements, and UCFS records the claim against it. The ARCVB runtime monitors and V&V harness feed the class society's surveyors rather than replace them. |
| Wedge limit | The specific mapping between UCFS and any class notation is open (UCFS v0.3 §1.8.5; open item K3 in Annex K). A class society that treats UCFS as competitive cannot be argued out of that position; the correct move is to invite them to define the mapping. That is a Phase 1 activity. The first concrete mapping task is UCFS claim classes against DNV AROS categories (remote control, decision support, supervised autonomy, full autonomy) and functions (navigation, engineering, operational, safety) [P]. |

#### 2.2.3 Defense acquisition and prime contractors

| Field | Value |
|---|---|
| Primary institutional fear | [P] Organisational fragmentation of autonomy programs and requirements locked in before the technology matures, slowing fielding (GAO-26-109014, June 2026). The earlier "crew checks not converted to software certification" hypothesis is not supported by the GAO material retrieved (Annex E). |
| What they actually need | [P] Ready-made V&V harnesses; incremental, evidence-bearing readiness gates (G0–G6) in place of fixed up-front requirements; common autonomy architectures that survive acquisition reviews |
| Architectural wedge | UCFS v0.3 §5 (gates G0–G6) with the v0.3 additions: G2 requires runtime monitor evidence (§5.2.4), G6 requires V&V results in the package (§5.2.5). ARCVB's V&V harness and runtime monitors map to G2 and G6 directly. |
| Wedge limit | UCFS v0.3 §24.4.1 downgrades the "runtime bridge" claim to [P] proposed — the ARCVB implementation has not been verified to perform it (open item K2). A prime contractor should be told this explicitly. The gates are a readiness framework, not a certification; the acquisition authority still evaluates. The IMO MASS Code excludes warships, so the defense wedge draws no authority from it. |

#### 2.2.4 Maritime counsel and insurers

| Field | Value |
|---|---|
| Primary institutional fear | [P] Unbounded civil liability under strict admiralty presumptions (e.g., *The Pennsylvania*, 86 U.S. (19 Wall.) 125 (1874) [P]; current application to be verified) and discoverability of internal risk memos |
| What they actually need | [P] Court-usable, tamper-evident telemetry; a strict separation between regulatory evidence and privileged legal analysis; a disclosure posture they can defend under discovery |
| Architectural wedge | UCFS v0.3 §26.8 (disclosure and privilege) with §26.8.3 (counsel sign-off criterion) and §26.5 (time architecture). The ledger is tamper-evident by a declared method (§26.6); the disclosure posture separates regulatory evidence, safety-management records, and privileged risk assessments; counsel sign-off is testable. |
| Wedge limit | UCFS does not claim court admissibility (§21.3, §26.7). It claims integrity and usability. Admissibility is a court decision, not a framework claim. Insurers must be invited to define their own acceptance criteria; IAAP does not assert what those criteria are. |

#### 2.2.5 Commercial autonomy developers (as adopters, not counterparties)

| Field | Value |
|---|---|
| Primary institutional fear | [P] Endless, expensive, case-by-case regulatory reviews; re-certification every time a software update ships |
| What they actually need | [P] Bounded pre-approval for routine parameter updates; a single standardized ConOps/Approval Basis schema that is accepted across ports and flags |
| Architectural wedge | UCFS v0.3 §18.2 (change classification) and §8.3.10 (status–compression mapping). The change classification separates minor bounded parameter updates (pre-approved within declared bounds) from behavior-altering changes (re-assessment). The status/compression mapping prevents the adopter from confusing "bounded" with "unconstrained." |
| Wedge limit | Whether an Administration will accept bounded pre-approval is unknown (UCFS v0.3 §18.2.2; open item K4). The framework offers the classification; it does not guarantee acceptance. A developer who assumes bounded pre-approval will be available is over-relying on the wedge. |

#### 2.2.6 Other counterparties (not surveyed)

**2.2.6.1** The matrix does not cover pilotage authorities, port State control officers, insurers' underwriters as distinct from counsel, class-society technical committees as distinct from class societies, or foreign flag-State authorities beyond the US/UK/Canada/Norway excerpts in the Bridge. These are open items (Annex B, B-1).

### 2.3 [P] discipline for the matrix

**2.3.1** Every [P] in §2.2 is a hypothesis about an institution's internal state, not a fact about it. The [P] flag is not a disclaimer; it is an instruction: validate before deploying.

**2.3.2** Validation routes for each [P] cell are listed in Annex A. The most common validation route is a first-meeting diagnostic (§3.1) in which the counterparty's own words about its pain points are recorded and the [P] hypothesis is updated.

**2.3.3** Where a [P] hypothesis is contradicted by a validation (e.g., a class society does not fear displacement but rather resource exhaustion), the wedge for that counterparty must be revised. That is a Phase 1 output, not a failure of IAAP.

---

## §3 — The Four-Phase Adoption Playbook

The phases are executed in strict sequence. Never skip Phase 1 to pitch Phase 3. Each phase has an objective, an action, a deliverable, and a negotiation rule. Each phase produces an artifact the next phase relies on.

### 3.1 Phase 1 — Zero-Threat Diagnostic

**3.1.1 Objective.** Enter the institution without triggering the "not invented here" immune response.

**3.1.2 Action.** Do not pitch the framework as a new rulebook or standard. Pitch a Friction & Gap Audit using the institution's own published pain points: GAO audit findings for defense and Coast Guard, Coast Guard Work Instruction 5P-WI-002(1) and 46 C.F.R. § 15.715 for the US flag-State context [P], IMO scoping gaps for the classification and regulatory context. The audit identifies specific, unresolved failure modes in the counterparty's current process — for example, "your current ConOps leaves Rule 17(b) prediction tolerances and SA-rebuild handover latency unquantified" (UCFS v0.3 §13.4, §14.1–14.2). A flag-State example [P]: "46 C.F.R. § 15.715 conditions acceptance of automation on demonstrated continuing reliability; your current submission format does not state how that is evidenced over time."

**3.1.3 Deliverable.** A 2–4 page diagnostic mapping the counterparty's current approval bottleneck to specific, unresolved failure modes. The diagnostic does not name UCFS, ARCVB, or IAAP unless the counterparty asks. Authorship and framework lineage MUST be disclosed on request and in any document the counterparty circulates onward (Rule 3); not naming the framework is a sequencing choice, not concealment.

**3.1.4 Negotiation rule.** Speak entirely in the counterparty's statutory and operational vocabulary. Let them recognize the problem before you show the engine. This is the phase where [P] hypotheses in §2.2 are validated (see §2.3.2): the counterparty's own words about its pain points are recorded and the matrix is updated.

**3.1.5 Failure modes for Phase 1.**

- Pitching the framework instead of the diagnostic (triggers the immune response; recovery requires starting over in a new meeting).
- Not validating [P] hypotheses (the later phases proceed on unfounded assumptions).
- Over-generalizing the diagnostic (a diagnostic that could apply to any institution is seen as a pitch in disguise).

### 3.2 Phase 2 — Declare the Limits Honestly

**3.2.1 Objective.** Establish durable credibility early in the technical review.

**3.2.2 Action.** Open with what the stack cannot do and what is not yet verified. Explicitly present:

- the [P] provisional flags from UCFS v0.3 §2.2;
- the NW non-waivable blockers (§5.4) and the reason they are blocked;
- the statuses that trigger Operation Not Permitted (§8.1.2–8.1.3);
- the open items in UCFS v0.3 Annex K (K1–K8) that the framework does not resolve;
- the framework's own limits (UCFS v0.3 §1.4, §2.3; IAAP v0.2 §1.4–1.5).

**3.2.3 Why this works.** It is not a technique. The limits are real. A sophisticated counterparty will see through a "declared limits" move that is deployed as a tactic, and will discount the declaration. The correct posture is: we declare the limits because they are the limits; here is exactly where the framework is strong and where it is provisional. Adopters who cannot adopt this posture are not ready for Phase 2.

**3.2.4 Deliverable.** A one-page "Limits Declaration" for the specific engagement, listing the specific [P] clauses, NW blocks, and open items that apply to this counterparty and this use case. The Limits Declaration is updated at each engagement and is a live document.

**3.2.5 Negotiation rule.** Do not soften the limits declaration under pressure. Softening it on the first challenge signals that the limits were a tactic; the counterparty will then treat every subsequent declaration as soft.

**3.2.6 Failure modes for Phase 2.**

- Presenting the limits as a technique ("and this is how we build trust") — the counterparty sees through it.
- Presenting all limits equally (the counterparty cannot tell which are material to their decision; the Limits Declaration must be specific to this counterparty).
- Retreating from a limit under challenge (destroys the credibility the phase was meant to build).

### 3.3 Phase 3 — Deliver a Real Legitimacy Win

**3.3.1 Objective.** Make the counterparty look competent to its own superiors by delivering an artifact that solves a real reporting or process problem.

**3.3.2 Action.** Hand over a modular artifact — the Annex A Claim Register, the G0–G6 Decision Gate Checklist, the NW non-waivable list as a review aid, or a ConOps/Approval Basis template — that solves an immediate, painful reporting problem for the individual in the room. The artifact must be usable independently of the rest of the stack. In the US flag-State context, a claim register structured around the 46 C.F.R. § 15.715 tests (capability, demonstrated continuing reliability, planned maintenance) is a candidate artifact [P].

**3.3.3 Real-win guard.** The artifact must reduce the counterparty's actual exposure, not merely appear to. A "legitimacy win" that is purely reputational — where the counterparty wraps the artifact in their branding without the artifact changing what they actually do — is a framing win, and it violates Rule 3 (Unimpeachable Provenance). If the artifact cannot reduce actual exposure, it is not ready for Phase 3, and Phase 1 or 2 must be revisited.

**3.3.4 Deliverable.** A specific artifact delivered to a specific individual with a specific use case. Artifacts are versioned and dated; the counterparty owns the artifact's use, not the framework's IP.

**3.3.5 Negotiation rule.** Allow the counterparty to wrap the architecture in their own branding, policy numbers, or internal workflows. The condition is that the underlying framework is genuinely being used — the artifact's structure must be visible in what the counterparty does, not only in the document's cover. Adopters retain ownership of the underlying specification and reference harness; the counterparty gets credit for solving an intractable bottleneck. Both claims are true only when the artifact is real.

**3.3.6 Failure modes for Phase 3.**

- Delivering a purely reputational win (violates Rule 3; the counterparty will not use the artifact and will not be protected by it).
- Delivering an artifact that requires the rest of the stack to be useful (the counterparty cannot use it; the win is not real).
- Delivering an artifact without version control (the counterparty cannot maintain it; the win decays).

### 3.4 Phase 4 — Lock the Interface

**3.4.1 Objective.** Turn one-off advisory work into a durable interface. When two or more entities use the claim structure to communicate, the schema becomes the de facto translation layer.

**3.4.2 Action.** Once two or more entities (e.g., a developer and a surveyor, or a defense lab and a testing range) use the claim structure to communicate, the schema has become an interface. Phase 4 stabilizes it.

**3.4.3 Stability commitment.** UCFS v0.3 §28.5: the framework MUST NOT update faster than an annual cadence for substantive revisions. Defect corrections are excepted and recorded (§28.5.1). UCFS v0.3 §28.5.2 declares v0.1→v0.2→v0.3 a single development cycle; the annual cadence begins at v0.3. [P] During the IMO experience-building phase (2026–28), operational evidence may argue for faster schema change than the annual cadence allows (Annex B, B-11).

**3.4.4 Reference Protocol Library.** UCFS v0.3 §28.7 (open item in the framework). Expansion of the reference library is the operational expression of Phase 4: every new user adds reusable derivation protocols, not gravity to an ecosystem.

**3.4.5 Deliverable.** A stable, versioned schema and a reference library that new adopters can use without renegotiating the interface.

**3.4.6 Negotiation rule.** The stability commitment is the adopter's credibility offer to the counterparty: we will not shift the schema unpredictably. That is the opposite of lock-in; it is a reliability guarantee. Adopters who cannot offer this — because their own frameworks are unstable — are not ready for Phase 4.

**3.4.7 Failure modes for Phase 4.**

- Claiming stability while changing the schema (destroys the interface; the counterparty cannot rely on it).
- Treating Phase 4 as a lock-in mechanism (violates Rule 1; the counterparty will exit).
- Expanding the library without version control (the reference protocols become unreliable).

---

## §4 — Pre-Engagement Gate Checklist

Every outgoing whitepaper, demo, Limits Declaration, diagnostic, or advisory pitch is run through these five gates before sending. The gates are self-audit checks, not institutional certifications. Passing them does not make an engagement safe; failing them makes it unsafe by IAAP's own standards.

### 4.1 Gate-to-rule mapping

| Gate | Rule it operationalizes | What it checks |
|---|---|---|
| I-1 | Rule 2 (Would It Help?) | Language discipline: no hype, no viral, no revolutionary |
| I-2 | Rule 1 (Asymmetric Empathy) | Counterparty exposure: the artifact reduces their risk |
| I-3 | Rule 3 (Unimpeachable Provenance) | Provisional honesty: [P] flags, placeholders, limits declared |
| I-4 | Rule 1 + Rule 4 (Asymmetric Empathy + Temporal Asymmetry) | Failure-first: leads with degradation behaviour, not ideal-condition performance; survives long wait cycles |
| I-5 | Rule 2 (Would It Help?) | Response preparation: targeted revisions ready, not defensive arguments |

### 4.2 Gate I-1 — Language discipline

- [ ] Have I removed all hype language ("revolutionary," "viral," "disruptive," "inescapable," "gravity," "unfair advantage," "game-changer") and replaced it with precise, RFC-2119-grade engineering claims?
- [ ] Does every claim that is an inference carry [P]?
- [ ] Does every clause that binds a counterparty use a modal term (MUST/SHOULD/MAY) in the RFC 2119 sense?
- [ ] Is "unique" absent unless accompanied by a specific difference from a named alternative?

### 4.3 Gate I-2 — Counterparty exposure

- [ ] Can I state in one sentence how adopting this artifact reduces the counterparty institution's exposure and gives the reviewing official a defensible administrative record?
- [ ] Does the sentence name the risk specifically (not "reputational" but "§ 8301 complement exposure")?
- [ ] Have I identified which institutional risk the counterparty carries, distinct from any individual risk?
- [ ] Is the artifact's protective value demonstrated, or only asserted?

### 4.4 Gate I-3 — Provisional honesty

- [ ] Are all unverified statutes, case-law analogies, and unvalidated thresholds explicitly tagged [P]?
- [ ] Are the [P] items that materially affect this counterparty's decision listed in the Limits Declaration (Phase 2)?
- [ ] Have I declared the framework's own open items (UCFS v0.3 Annex K, IAAP Annex B) that bear on this engagement?
- [ ] Have I stated what this artifact cannot do, in the same document as what it can?
- [ ] Is authorship and framework lineage disclosed on request, and carried in any document the counterparty may circulate onward?

### 4.5 Gate I-4 — Failure-first (survives the wait)

- [ ] Does the presentation lead with how the system detects its own failure and degrades safely (UCFS v0.3 §24), rather than with how well it works under ideal conditions?
- [ ] Does the artifact survive a 12-month wait without requiring rework? (UCFS v0.3 §28.5 stability commitment; §28.5.2 single-cycle declaration)
- [ ] Are the runtime monitors and escalation routes specified at the level a counterparty would need to see them working (§5.2.4)?
- [ ] Are the degraded-state transitions (§12.4, §14.1) described as specific behaviours, not as "graceful degradation" in the abstract?

### 4.6 Gate I-5 — Response preparation

- [ ] If the counterparty pushes back on a premise, is my prepared response a targeted architectural revision (a clause change, a clause reference, a Limits Declaration update), rather than a defensive argument?
- [ ] Have I identified the three most likely objections for this counterparty and prepared a specific revision for each?
- [ ] Is my prepared response compatible with Rule 3 (does not over-claim to answer the objection)?
- [ ] Have I written down what I would change about the stack if the objection is correct? (If nothing, the objection is not really being engaged.)

### 4.7 Record

**4.7.1** The five gates are checked before each outgoing engagement and the result is recorded. A pass on gate I-1 does not imply a pass on I-2; each gate is independent.

**4.7.2** Failure of any gate is a signal to revise the artifact, not the gate. The gates are the standard; the artifact is the variable.

---

## §5 — Failure Paths and Refusal Protocols

The four-phase playbook assumes the counterparty is engaged. Institutions sometimes refuse. IAAP must say what to do when they do.

### 5.1 Refusal at Phase 1 (diagnostic rejected as a pitch in disguise)

**5.1.1** Recovery: return to the diagnostic's evidence base and present the specific GAO report, work instruction, or IMO scoping gap that the diagnostic relies on. The diagnostic is not a pitch; it is a reading of the counterparty's own published pain points.

**5.1.2** If the diagnostic is still rejected, the counterparty is not ready for Phase 1. There is no Phase 0. Withdraw and return only when the counterparty's own published pain points have changed, or when a new individual occupies the decision role.

### 5.2 Refusal at Phase 2 (limits declaration rejected as a tactic)

**5.2.1** Recovery: ask the counterparty what they would need to see to accept that the limits are real. This is a genuine request, not a tactic. If the counterparty names a specific test, run it. If they name a class of tests, propose one.

**5.2.2** If the counterparty cannot name what would convince them, the failure is at the counterparty's process, not at the adopter's declaration. Record it and withdraw.

### 5.3 Refusal at Phase 3 (legitimacy win dismissed as reputational)

**5.3.1** Recovery: the real-win guard was not met. Return to Phase 1 or 2 and produce a different artifact that reduces the counterparty's actual exposure.

**5.3.2** If no such artifact exists, the counterparty has no pain point that the stack addresses. IAAP's role is to not deploy, not to fabricate a need.

### 5.4 Refusal at Phase 4 (interface lock refused)

**5.4.1** A class society that treats UCFS as competitive rather than complementary will refuse Phase 4. This is a structural outcome, not a negotiation failure. Options:

- Invite them to define the mapping (UCFS v0.3 §1.8.5, open item K3). The class society's own mapping is more durable than one proposed by the adopter.
- Accept parallel use — UCFS alongside the class notation, not replacing it. The claim register records against the notation; the notation governs technical requirements (§1.8.4).
- Withdraw and wait for the class society to develop its own autonomy notation and invite mapping.

**5.4.2** A flag-State administration that will not accept UCFS has statutory authority over the vessel, not over the framework. The framework is not a regulatory submission; it is a claim-and-evidence structure. The administration may accept some claims and reject others; the adopter's task is to make the rejected claims visible to the adopter (as open residues), not to argue the administration out of its position.

### 5.5 Regulator non-recognition across ports

**5.5.1** A vessel approved under one flag may arrive in a port whose Port State Control officers do not recognize the approval basis. IAAP cannot solve this; it is a structural problem noted in the Bridge and in UCFS v0.3 §19.4 (PSC interface).

**5.5.2** The adopter's response is not to argue PSC recognition, but to prepare the PSC approval passport (UCFS v0.3 §19.4) — a summary the master or ROC can produce to a PSC officer on request — and to accept that some ports will require re-review. This is an open item (Annex B, B-2).

### 5.6 What to do with a refusal

**5.6.1** Record the refusal in the adopter's engagement log, with the counterparty, the phase, the stated reason, and the adopter's assessment.

**5.6.2** A refusal at any phase is not a personal rejection. It is input telemetry (Rule 2). The engagement log is the mechanism that turns refusals into usable information about which counterparties are ready and which are not.

**5.6.3** A refusal does not authorize misrepresenting the framework, softening the limits declaration, or fabricating a legitimacy win. Those are Rule 3 violations and they destroy the adopter's credibility across all counterparties, not just the refusing one.

---

## §6 — Stack Integration

IAAP sits above UCFS v0.3, ARCVB and the MASS Regulatory Bridge. The layers are:

```
+-------------------------------------------------------------------+
| LAYER 4: IAAP v0.2.1 (Institutional Alignment & Adoption Protocol)|
| -> How the stack is negotiated, sequenced and deployed.          |
+-------------------------------------------------------------------+
                                  |
                                  v
+-------------------------------------------------------------------+
| LAYER 3: UCFS v0.3 (Uncertainty Compression Framework/Spec)       |
| -> The normative rules, gates, vectors and evidence tiers.       |
+-------------------------------------------------------------------+
                                  |
                                  v
+-------------------------------------------------------------------+
| LAYER 2: ARCVB (Automated Regulatory Compliance & V&V Bridge)     |
| -> Runtime monitors, state machines, harness, ledger.            |
+-------------------------------------------------------------------+
                                  |
                                  v
+-------------------------------------------------------------------+
| LAYER 1: MASS Regulatory Bridge (13 Nov 2026 Working Paper)       |
| -> The legal, statutory and case-law friction map.               |
+-------------------------------------------------------------------+
```

### 6.1 UCFS v0.3 clauses IAAP depends on

**6.1.1** The following UCFS v0.3 clauses are operative dependencies of IAAP v0.2. IAAP MUST be re-reviewed whenever any of them changes materially.

| UCFS v0.3 clause | What it establishes | How IAAP uses it |
|---|---|---|
| §1.4 (limits) | Framework is not a compliance guarantee | Bounds the Phase 2 limits declaration |
| §1.8 (complementarity) | UCFS is a claim layer, not a rule set | The class-society wedge (§2.2.2) |
| §2.2 ([P] clearing) | Two routes for clearing [P] | Phase 2 declaration (§3.2) |
| §4.2 (vector) | Vector is measurement; conformance is separate | Flag-State wedge (§2.2.1) |
| §5 (gates G0–G6) | Decision gates and severity classes | Defense wedge (§2.2.3); Phase 4 interface (§3.4) |
| §5.4 (NW list) | Non-waivable domains; bounded claims S2 | Flag-State wedge (§2.2.1); Phase 2 limits (§3.2) |
| §8.1.2–8.1.3 (Operation Not Permitted) | Failed claims suspend approval | Phase 2 limits (§3.2) |
| §8.1.4 (failed → bounded) | Conversion changes compression type and status | Commercial developer wedge (§2.2.5) |
| §8.3.10 (status–compression mapping) | The two attributes are separated | Commercial developer wedge (§2.2.5) |
| §8.5.6 (E4 obligation) | E4 is defined | Phase 4 stability (§3.4) |
| §8.8 (severity classes) | S1/S2/S3 | Phase 2 limits (§3.2) |
| §8.11 (confidence bands) | Band and derivation protocol | Phase 2 limits (§3.2) |
| §12.1 (Rule 5 application + interpretation) | Dual compression set | Limits declaration when applicable |
| §13.4, §14.1–14.2 (Rule 17(b), handover) | Specific unquantified gaps | Phase 1 diagnostic (§3.1) |
| §18.2 (change classification) | Bounded pre-approval structure | Commercial developer wedge (§2.2.5) |
| §19.4 (PSC interface) | PSC passport requirement | Failure path (§5.5) |
| §21.3 (admissibility limit) | Investigator-usable, not court-admissible | Counsel/insurer wedge (§2.2.4) |
| §24 (runtime claim validity) | Runtime monitors; §24.4.1 [P] proposed | Defense wedge (§2.2.3); Phase 2 (§3.2) |
| §26.5–26.8 (ledger, time, disclosure) | Tamper-evidence and privilege | Counsel/insurer wedge (§2.2.4) |
| §28.5, §28.5.1, §28.5.2 (stability) | Annual cadence; defect correction; single-cycle declaration | Phase 4 stability (§3.4) |
| §28.6 (conformance mark suspended) | Mark unavailable | Not referenced; IAAP does not use the mark |
| Annex K (open items K1–K8) | Framework-level open items | Phase 2 limits declaration (§3.2) |

### 6.2 UCFS v0.3 clauses IAAP does not depend on

**6.2.1** IAAP does not depend on UCFS's internal evidentiary clauses (§7 operators, §8.6 derivation protocol, §9 invariants, §10–23 domain clauses) except where cited in §6.1. IAAP is a negotiation layer; it does not resolve technical claims.

**6.2.2** IAAP does not depend on the ARCVB implementation. §24.4.1's runtime-bridge claim is [P] proposed (open item K2); IAAP does not assert the bridge exists, only that it is what the defense wedge would rely on if it does.

### 6.3 What IAAP does not integrate

**6.3.1** IAAP does not integrate with class-society rulebooks (open item K3) beyond the general complementarity in §1.8.

**6.3.2** IAAP does not integrate with any national regulatory scheme directly; it is a proposal layer, not a filing layer.

**6.3.3** IAAP does not integrate with insurers' underwriting models; the counsel/insurer wedge is advisory to counsel and insurers, not a direct interface.

---

## §7 — Governance and Stability

### 7.1 Version discipline

**7.1.1** IAAP versions follow the same discipline as UCFS (§28.5, §28.5.1, §28.5.2). Substantive revisions are gated to an annual cadence; defect corrections are recorded in §0 of the current version.

**7.1.2** IAAP v0.1 → v0.2 is a defect correction and structural revision (version alignment, renamings, added sections, failure paths, [P] discipline, gate mapping). It is not a substantive revision under §28.5.

**7.1.3** The next IAAP version (v0.3) would be the candidate for a substantive revision. It is not scheduled.

**7.1.4** IAAP v0.2 → v0.2.1 is a defect correction and [P] evidence update (§0.5). It is not a substantive revision under §28.5.

### 7.2 Stability commitment to counterparties

**7.2.1** IAAP's version discipline is itself a claim to counterparties: the negotiation protocol will not shift unpredictably. This is the same guarantee UCFS v0.3 §28.5 makes about its own claims, applied at the negotiation layer.

**7.2.2** A counterparty that has engaged via IAAP v0.2 and is facing a future IAAP v0.3 can rely on:

- the four rules (§1.2) remaining the operative philosophy;
- the four-phase playbook (§3) remaining the operative sequence;
- the five pre-engagement gates (§4) remaining the operative self-audit;
- the [P] discipline (§2.3) remaining in force.

**7.2.3** A counterparty cannot rely on any specific wording remaining unchanged across a substantive revision. That is the same limitation UCFS v0.3 §28.5 imposes on itself.

### 7.3 Provenance and independent review

**7.3.1** IAAP v0.2 is produced by the same collaborator as UCFS v0.2, UCFS v0.3 and the UAIRF v1.1 review. It is development evidence, not independent corroboration (§1.5.1).

**7.3.2** IAAP v0.2 has not been reviewed under UAIRF v1.1. A full UAIRF review and an external practitioner review are open items (Annex B, B-9).

**7.3.3** IAAP v0.2 has not been tested in any institutional engagement. Adoption results would be evidence; the protocol itself is not.

### 7.4 What IAAP claims and does not claim

**7.4.1** IAAP claims: a coherent protocol for presenting, sequencing and negotiating the UCFS/ARCVB stack across institutions, with the four rules (§1.2), the counterparty matrix (§2), the four-phase playbook (§3), the five pre-engagement gates (§4), and the failure paths (§5).

**7.4.2** IAAP does not claim: institutional endorsement; adoption; recognition; that any specific counterparty will accept any specific wedge; that the counterparty fears in §2.2 are correct; that the UCFS/ARCVB stack is complete.

**7.4.3** IAAP MUST NOT be cited as evidence that any institution will accept any part of the stack. It is a protocol; the institution decides.

### 7.5 External timeline (as of 14 Nov 2026) [P]

**7.5.1** The following dates come from secondary sources (Annex E) and MUST be re-verified before use in any engagement.

| Date | Event |
|---|---|
| 13–22 May 2026 | IMO MSC 111 adopts the non-mandatory MASS Code |
| 1 Jul 2026 | MASS Code takes effect (non-mandatory) |
| Dec 2026 | MSC 112 expected to re-establish the MASS working group to frame the experience-building phase (EBP) |
| 2026–2028 | Experience-building phase |
| 2028 | Development of the mandatory code begins; SOLAS amendments (a new chapter) considered |
| 1 Jul 2030 | Target adoption of the mandatory code |
| 1 Jan 2032 | Target entry into force, at the earliest; IMO noted the timeline may be revisited |

**7.5.2** [P] Inference: the EBP window is the most direct route for operational evidence from Phase 1 diagnostics and Phase 3 artifacts to reach IMO discussion, through flag States. IAAP does not assume any flag State will submit such evidence.

---

## Annex A — [P] Register

Every [P] hypothesis in §2.2 and every [P] dependency in §6.1 is listed here, with its validation route.

| # | [P] hypothesis | Location | Validation route |
|---|---|---|---|
| A-1 | Flag-State administrations fear casualty-approval, statutory violation, and inconsistent port-to-port rulings | §2.2.1 | Phase 1 diagnostic; validate with specific officials. Statutory-floor element supported by USCG Work Instruction 5P-WI-002(1) (Annex E); port-to-port element unverified |
| A-2 | Flag-State administrations need a repeatable administrative record | §2.2.1 | Same as A-1 |
| A-3 | Classification societies fear parallel-framework fragmentation and notation undermining (revised from "displacement" in v0.2; societies are launching their own autonomy notations) | §2.2.2 | Phase 1 diagnostic with the specific society's technical committee; start with DNV AROS |
| A-4 | Classification societies need to preserve their notation as authoritative and to see UCFS claims map onto it | §2.2.2 | Same as A-3 |
| A-5 | Defense acquisition suffers organisational fragmentation and early requirement lock-in (replaces the v0.2 "idle hulls / un-converted crew checks" hypothesis, which the retrieved GAO material does not support) | §2.2.3 | GAO-26-109014 (read the full body, Annex B B-12); validate with acquisition offices |
| A-6 | Defense acquisition needs V&V harnesses and incremental readiness gates | §2.2.3 | Same as A-5 |
| A-7 | Maritime counsel and insurers fear *Pennsylvania* exposure and discoverability | §2.2.4 | Phase 1 diagnostic with counsel; validate with underwriters separately |
| A-8 | Counsel and insurers need tamper-evident telemetry and privilege separation | §2.2.4 | Same as A-7 |
| A-9 | Commercial developers fear case-by-case re-certification | §2.2.5 | Phase 1 diagnostic with developers; validate per jurisdiction |
| A-10 | Commercial developers need bounded pre-approval and standardized schema | §2.2.5 | Same as A-9 |
| A-11 | UCFS v0.3 §24.4.1 runtime bridge is proposed, not verified | §6.1 | Open item K2; verify against ARCVB implementation |
| A-12 | *Ever Smart* (*Evergreen Marine (UK) Ltd v Nautical Challenge Ltd* [2021] UKSC 6; crossing rules held to apply; apportionment re-determined at [2022] EWHC 206 (Admlty)) is persuasive in common-law jurisdictions only | §6.1 (via UCFS v0.3 §11.1.1) | Verify per operating jurisdiction before Class C+ claim |
| A-13 | The IMO experience-building phase (2026–28) is the most direct route for operational evidence to reach IMO discussion | §7.5 | Confirm with a flag-State administration; MSC 112 outcome (Dec 2026) |

A [P] hypothesis contradicted by validation must be revised, and the counterparty wedge in §2.2 must be revised with it. The [P] register is a live document.

---

## Annex B — Open Items

The following cannot be resolved within IAAP v0.2 without information or decisions not available to this draft.

| # | Open item | Why it is open | Owner |
|---|---|---|---|
| B-1 | Validation of counterparty-fear hypotheses for institutions beyond the four surveyed (US, UK, Canada, Norway) | No survey of these institutions has been conducted | Adopter + Phase 1 diagnostic |
| B-2 | Port State Control recognition across ports | A structural problem; UCFS v0.3 §19.4 requires a PSC approval passport; IAAP cannot guarantee recognition | Flag State; PSC regimes |
| B-3 | Class-society mapping for UCFS | UCFS v0.3 §1.8.5 and Annex K3; not resolved in the framework. First task: DNV AROS categories and functions | Class societies; adopter |
| B-4 | Whether Administrations will accept bounded pre-approval | UCFS v0.3 §18.2.2; open item K4 | Administrations |
| B-5 | Whether any institution will accept a diagnostic that does not name UCFS/ARCVB | Phase 1 is untested | Adopter's engagement log |
| B-6 | Whether the "declared limits" move in Phase 2 is sustainable under challenge | Phase 2 is untested | Adopter's engagement log |
| B-7 | Whether the "real-win" guard in Phase 3 is sufficient against reputational-only wins | Not tested against a counterparty inclined to framing | Adopter's engagement log |
| B-8 | Whether Phase 4's stability commitment survives a substantive UCFS revision | UCFS v0.3 is the first version under the stability commitment; no revision has yet exercised it | UCFS governance |
| B-9 | A full UAIRF v1.1 review of IAAP, plus an external practitioner review (marine safety inspector, surveyor or admiralty counsel) of the Limits Declaration and Phase 1 template | Not performed; a UAIRF pass alone is another same-collaborator review | Author; external reviewer |
| B-10 | A tested pilot of the full four-phase playbook with a real institution | Not performed; the protocol is proposed, not demonstrated | Adopter |
| B-11 | Whether the annual cadence (UCFS v0.3 §28.5) is compatible with feedback from the IMO experience-building phase | Operational evidence during 2026–28 may argue for faster schema change | UCFS governance |
| B-12 | Primary-text verification of every Annex E item | Annex E was built from secondary sources and search summaries | Author |

An open item is not an unresolved defect in IAAP. It is a question IAAP does not answer, recorded so it is not silently dropped.

---

## Annex C — Lineage Declaration

**C.1 Comparison method.** IAAP v0.1 → v0.2 was compared by itemised carry-forward list. Every v0.1 section was checked against a v0.2 section; renaming and structural changes are recorded in §0.

**C.2 No silent drops.** The v0.2 revision claims no silent drops of v0.1 content. The specific changes are: version alignment (§0.1), renaming of the role line and Phase 1 (§0.2.1–0.2.2), removal of "inescapable" and "gravity" language (§0.2.3), renaming of Phase 2 (§0.2.5), fixed gate numbering (§0.3.1), gate-to-rule mapping (§0.3.2), real-win guard (§0.3.3), failure paths (§0.3.4), [P] discipline (§0.3.5), provenance/limits (§0.3.6), governance (§0.3.7), and the new annexes A–D.

**C.3 Scope of the claim.** The "no silent drops" claim is a completeness claim. Its method is the itemised carry-forward list; its limit is that the comparison was performed by the same collaborator as v0.1. Under UAIRF §26.6, the method is declared and the limit is stated; the claim is supported at the stated limit, not beyond it.

**C.4 What v0.2 retains from v0.1.** The four architectural rules (§1.2), the counterparty categories (§2.2, though expanded and [P]-tagged), the four-phase playbook (§3, with Phase 1 and Phase 2 renamed and Phase 3 given a real-win guard), and the pre-engagement checklist (§4, with numbering fixed and rule mapping added).

**C.5 What v0.2 adds.** Version alignment (§0.1, §6.1), limits section (§1.4–1.5), [P] discipline (§2.3), failure paths (§5), stack integration with explicit UCFS v0.3 clause references (§6), governance (§7), [P] register (Annex A), open items (Annex B).

**C.6 v0.2 → v0.2.1.** Compared by itemised list (§0.5 and the second table in Annex D). Nothing from v0.2 was dropped. Changed text is either corrected (§1.4.3, A-3 to A-6, Gate I-2) or extended (§3.1.3, §7.5, Annexes A, B and E). The comparison was done by the same collaborator as v0.2; the limit in C.3 applies.

---

## Annex D — Resolution log for v0.1 → v0.2

Every substantive change is recorded here, with the reason.

### v0.1 → v0.2

| # | Change | Reason |
|---|---|---|
| R-1 | Role line: "gatekeeper-bypass specification" → "institutional alignment, stakeholder negotiation and interface specification" | Bypass framing contradicts Rule 1 and Rule 3; will be read as hostile by counterparties |
| R-2 | "Trojan Horse Diagnostic" → "Zero-Threat Diagnostic" | The Trojan Horse myth is bluff-and-conquer; naming a phase after it costs first-meeting credibility |
| R-3 | "inescapable industry standard" and "gravity" → stability commitment language | Same family as "viral"; Gate I-1 removes it |
| R-4 | "Surrender the High Ground" → "Declare the Limits Honestly" | The technique framing invites suspicion; the limits are real, not tactical |
| R-5 | "gatekeeper" retained only as a general term; "counterparty", "co-regulator", "co-standards-setter" used for specific institutions | Outsider framing costs adoption |
| R-6 | UCFS version references updated from v0.2 to v0.3 | Version discipline |
| R-7 | §5.4 (NW list), §4.2 (vector), §5.2 (gates), §26.8 (disclosure), §28.5 (stability), §28.6 (conformance mark), §24.4 (runtime bridge) — all materially changed in v0.3 | IAAP must reference the v0.3 forms |
| R-8 | §24.4.1 runtime bridge [P] proposed — declared in Phase 2 limits | UCFS v0.3 downgraded the bridge claim |
| R-9 | §28.6 conformance mark suspended — IAAP does not reference it | Mark unavailable until Annex I is populated |
| R-10 | Gate numbering fixed to I-1 through I-5 | Schema consistency |
| R-11 | Gate-to-rule mapping added (§4.1) | The five gates and four rules were not mapped |
| R-12 | Phase 3 real-win guard added | Legitimacy win without real exposure reduction violates Rule 3 |
| R-13 | Failure paths added (§5) | Playbook assumed adoption; refusals were unaddressed |
| R-14 | [P] discipline for counterparty fears added (§2.3, Annex A) | Counterparty fears are hypotheses, not facts |
| R-15 | Limits section added (§1.4–1.5) | IAAP is most exposed to being read as manipulation manual |
| R-16 | Provenance note added (§1.5, §7.3) | Same-collaborator production |
| R-17 | Open items register added (Annex B) | Other layers in the stack have one |
| R-18 | Lineage declaration added (Annex C) | Version discipline |
| R-19 | §6.1 UCFS v0.3 clause dependency table added | Every dependent clause is named; version re-referencing is auditable |
| R-20 | §6.2 explicit statement of what IAAP does not depend on | Prevents over-claiming the integration |
| R-21 | §7 governance added | Annual cadence, defect correction, single-cycle declaration |
| R-22 | Notice block added | Every other stack document has one; IAAP is most exposed |
| R-23 | §0.4 non-adoption of a full UAIRF review recorded | Recorded, not silently dropped |

### v0.2 → v0.2.1

| # | Change | Reason |
|---|---|---|
| R-24 | §1.4.3 corrected: MASS Code is non-mandatory; approval is national | MASS Code adopted as non-mandatory, effective 1 Jul 2026 (Annex E) |
| R-25 | Dated IMO timeline added (§1.2.4, §3.4, §7.5, A-13) | Gives Rule 4 concrete dates; [P] |
| R-26 | USCG WI 5P-WI-002(1) and 46 C.F.R. § 15.715 named (§2.2.1, §3.1, §3.3) | Replaces the generic "Coast Guard work instructions" |
| R-27 | Class-society fear and wedge limit revised; B-3 names DNV AROS (§2.2.2, A-3, A-4) | Societies are launching their own autonomy notations |
| R-28 | Defense fear and needs revised; MASS Code warship exclusion noted (§2.2.3, A-5, A-6) | Retrieved GAO finding is organisational, not crew-check conversion |
| R-29 | *Ever Smart* citation added; *The Pennsylvania* cited and tagged [P] (A-12, §2.2.4) | Grounding |
| R-30 | Provenance disclosure added (§3.1.3, Gate I-3) | Not naming the framework must not become concealment (Rule 3) |
| R-31 | Gate I-2 reworded to institutional exposure and defensible record | Original wording could read as offering personal cover |
| R-32 | External practitioner review added (B-9, §7.3.2) | A UAIRF pass alone is another same-collaborator review |
| R-33 | §3 paragraphs numbered; §0.3.3 reference corrected to §3.3.3 | Dangling §3.3.4 reference |
| R-34 | Annex D added to §0.1.3; Annex E added | Completeness |
| R-35 | "within the first ten minutes" removed from Phase 2 | Unsupported figure |
| R-36 | B-11 (cadence vs experience-building feedback) and B-12 (primary-text verification) added | Open questions recorded, not dropped |
| R-37 | Layer-diagram label updated to v0.2.1 | Version alignment |

---

## Annex E — Evidence base (retrieved 14 Nov 2026)

All items are [P]: secondary sources or search summaries, not primary texts. Verification is tracked at B-12.

| # | Finding | Source |
|---|---|---|
| E-1 | MASS Code adopted at MSC 111 (13–22 May 2026) as a non-mandatory instrument, effective 1 Jul 2026 | hellenicshippingnews.com/imo-msc-111-new-mass-code-adopted/; news.uscg.mil (Maritime Commons) |
| E-2 | Experience-building phase 2026–28; MSC 112 (Dec 2026) re-establishes the MASS working group; mandatory-code work from 2028; adoption target Jul 2030; entry into force 1 Jan 2032 at the earliest, possibly revisited; likely a new SOLAS chapter | hilldickinson.com; natlawreview.com; hellenicshippingnews.com |
| E-3 | Code is goal-based, applies to cargo ships, excludes warships, requires human oversight and control (Art. 8.7), and mostly addresses risks to MASS systems rather than risks caused by them | cil.nus.edu.sg (analysis of MSC 111/5/3) |
| E-4 | USCG Work Instruction 5P-WI-002(1) cancels CVC Policy Letter 22-01 (Change 1); OCMI retains final authority; manning not below 46 U.S.C. § 8301 and 46 C.F.R. Part 15; cites NDAA FY2026 (Pub. L. 119-60) | dco.uscg.mil (work instruction text); natlawreview.com |
| E-5 | 46 C.F.R. § 15.715: acceptance of crew-replacing automation rests on capability, demonstrated continuing reliability and a planned maintenance regime | federal-regs.com/title/46/part-15/15.715/ |
| E-6 | DNV AROS notations available since 1 Jan 2025: four functions by four categories, aligned to MASS Code definitions, building on DNV-CG-0264 | dnv.com; oceannews.com |
| E-7 | Other class activity: Bureau Veritas approval in principle for Greenroom Robotics autonomy software (Feb 2026); ABS approvals in principle for autonomy frameworks (2025) | thedigitalship.com; marinelink.com (headline-level only) |
| E-8 | GAO-26-109014 (15 Jun 2026): leadership and organisational challenges; domain silos; requirements set too early for LUSV and XLUUV; Navy PAE RAS created Dec 2025; "marketplace" approach for MUSV | gao.gov/products/gao-26-109014; maritime-executive.com; navytimes.com |
| E-9 | *Evergreen Marine (UK) Ltd v Nautical Challenge Ltd* [2021] UKSC 6 (19 Feb 2021): crossing rules held to apply to the 2015 Jebel Ali collision; apportionment re-determined at [2022] EWHC 206 (Admlty) | supremecourt.uk; caselaw.nationalarchives.gov.uk |
| E-10 | *The Pennsylvania*, 86 U.S. (19 Wall.) 125 (1874): cited from general knowledge, not retrieved | none retrieved; verify |

Not covered: UK MCA, Transport Canada (a Tier 1 autonomous-navigation policy appeared in one result), Norway, and the detail of the BV and ABS approvals in principle.

---

## Closing note

IAAP v0.2 is a defect correction and structural revision, not a substantive revision. It fixes what the same review that produced UCFS v0.3 surfaced in IAAP v0.1: version mismatch, framing problems, missing failure paths, and missing [P] discipline.

Two things remain genuinely open and are recorded in Annex B rather than addressed:

1. No institution has been engaged via this protocol in a documented way. IAAP is proposed, not tested.
2. No full UAIRF v1.1 review of IAAP has been performed. The protocol that has been applied to UCFS v0.2 has not been applied to IAAP itself.

Both are honest limits. An adopter who runs the protocol with these limits declared is doing what the protocol says to do. An adopter who claims the protocol is validated has not read §1.5.

The next steps, if you want them, are: (1) check every Annex E item against its primary text (B-12); (2) have an external practitioner read the Limits Declaration and Phase 1 template for realism; (3) then run a full UAIRF v1.1 pass on IAAP v0.2.1. Together these would close open item B-9 and would produce a v0.3 finding register.
