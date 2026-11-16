# UCFS v0.3.1 — Uncertainty Compression Framework/Spec

**Parent specification for the Automated Regulatory Compliance & Verification Bridge (ARCVB)**

| Field | Value |
|---|---|
| Document | UCFS v0.3.1 — full normative specification (defect-correction release of v0.3; no clause renumbered) |
| Supersedes | UCFS v0.3 and v0.2 |
| Revision type | Defect correction under §28.5.1: annex corrections, new open items and watch items, and a non-operative proposals annex (Annex P). No operative clause is added, changed or removed. See §0.4. |
| Status | Draft for technical review. Not a standard. Not legal advice. Not endorsed by any Administration, recognized organization or classification society. Not a basis for certification. |
| Relationship | Parent specification. ARCVB is the implementation pipeline; the MASS Regulatory Bridge (13 Nov 2026) is the friction and evidence source map. |
| Conventions | MUST, MUST NOT, SHOULD, SHOULD NOT, MAY in the RFC 2119 sense. |
| Provisional flag | **[P]** marks a clause resting on an unverified source. A [P] clause cannot support a conformance claim until the source is verified or the approval authority has accepted the [P] status under §2.4. |
| Change basis | UAIRF v1.1 application to UCFS v0.2 (14 November 2026). Findings F1–F30 addressed; open items carried to Annex K. |

> **Build note.** This file merges the v0.3 text with the full v0.2 text for every section that v0.3 marked "unchanged from v0.2". Merged v0.2 text is reproduced verbatim (tables converted to Markdown, bullets normalised). Where v0.3 states a change, the v0.3 wording governs. Cross-reference and consistency problems found during the merge are listed in **Annex Z (editorial, non-normative)** at the end; the body text has not been altered to fix them.

---

## 0. Changes from v0.2 and resolution log

### 0.1 Fixes applied (v0.2 → v0.3)

**0.1.1 Schema reconciliation (F1, F2, F11, F29, F30).** The claim model's "compression type" and "status" attributes are separated with a declared combination rule (§3.6–3.10, §8.2, §8.3). A claim MAY carry a compression type set (ordered) when a single claim genuinely rests on two modes; the set carries a declared priority. "Bounded fallback" is a compression type; "bounded" is a status. The mapping is declared in §8.3.10. The Rule 5 "application + interpretation" dual is permitted as a compression type set (§12.1).

**0.1.2 Non-waivable severity reconciliation (F3, F16).** §5.4.2 is revised: a residue in a non-waivable domain is S1; a bounded claim in a non-waivable domain is S2 with a mandatory runtime escalation (§8.10.3). The two clauses no longer conflict. §8.8.3 is reformulated to one rule.

**0.1.3 E4 obligation defined (F4, F26).** The "E4 obligation" is defined in §8.5.6: a data-collection plan, a reporting cadence, a re-assessment trigger, a declared fallback if E4 evidence does not materialize, and an owner.

**0.1.4 Off-list non-waivable domains (F5).** Submitters MUST identify any non-waivable domain under the flag State's law not on the UCFS list (§5.4.3).

**0.1.5 Conformance vector separated from conformance claim (F6).** The vector is a measurement (§4.2.1). Conformance is a separate gate-based claim (§4.1.1). The small-operator vector (§4.3.1) is a measurement, not a conformance claim.

**0.1.6 Runtime monitors gated (F7, F23).** A new decision gate requirement at G2 requires runtime monitor specifications and test evidence (§5.2.4). §24.4's "bridge" claim is downgraded to a proposed claim (§24.4.1).

**0.1.7 Uncertainty propagation derivation (F8).** The propagation model must carry a derivation protocol (§9.5.1).

**0.1.8 V&V results in package (F9).** V&V results with evidence tiers are a package requirement at G6 (§5.2.5, §27.9).

**0.1.9 Conformance mark disabled until policy exists (F10).** §28.6 is suspended; "UCFS-conformant" MUST NOT be claimed until Annex I is populated (§28.6.1).

**0.1.10 N/A failure mode (F12).** N/A claims are exempted from the failure-mode attribute; the reverse-evidence trigger is declared instead (§8.4.3).

**0.1.11 Evidence sub-items declared (F13).** D-C and D-D sub-items are declared in §6.4.1 and §6.4.2 so the evidence-tier table (§8.5.5) has referents.

**0.1.12 Ever Smart persuasive claim narrowed (F14).** §11.1 revised; [P] flag applied to the persuasive claim, not only to the paragraph numbers.

**0.1.13 Rule 19 fusion state derivation (F15).** §12.6.2 requires a derivation protocol for the fusion state.

**0.1.14 Annex E conditional severities removed (F17).** E8 and E10 are stated as S1 unconditionally.

**0.1.15 Civil-military removed from Annex E (F18).** Retained only in Annex H, consistent with §20.5.

**0.1.16 Annex J M-items addressed individually (F19).** Annex J is restructured to name the specific clause for each M item, or to record the item as an open item in Annex K.

**0.1.17 [P] clearing procedure (F20).** §2.2 provides two routes: verification by the submitter (with a verification record), or approval-authority acceptance of the [P] status (with a recorded acceptance). The framework no longer blocks all approval packages that rely on [P] claims.

**0.1.18 Confidence-band method (F21).** §8.11.5 requires a derivation protocol for the confidence band.

**0.1.19 Disclosure acceptance criterion (F22).** §26.8.3 defines the testable criterion.

**0.1.20 §26.7 / §26.8 reconciliation (F24).** §26.7 is qualified: availability is subject to the declared privilege posture.

**0.1.21 Dimension independence (F25).** §4.2.4 acknowledges the overlap between C and P and between B and V; the vector is not fully orthogonal.

**0.1.22 Lineage declaration (F27).** Annex L declares the comparison method from v0.1 → v0.2 → v0.3.

**0.1.23 Internal authority field for non-hierarchical documents (F28).** Not resolved. No clause for this exists in v0.2 or v0.3; the item is recorded as open item K12 (Annex K), not as a fix.

**0.1.24 COLREG equivalence route (F30).** Recorded as an open item (§K1). UCFS does not assert whether COLREG has an equivalence route.

**0.1.25 Annual-cadence self-violation (U4 in the review).** §28.5 is revised: the annual cadence applies to substantive revisions, not to defect corrections, and v0.1 → v0.2 → v0.3 are declared as a single development cycle (§28.5.2).

**0.1.26 MSC.595(111) [P] vs Bridge verification (GS2).** The [P] flag is retained with an explicit note: the Bridge marks this source verified, but the operative text was not re-read in preparing UCFS. §2.3 requires the submitter to reconcile the two statuses.

**0.1.27 Merge corrections (post-merge review).** Definitions of closed, bounded and failed restored (§3.35–3.37) and the compression caution restored (§3.4.1); open items K9–K12 added; the "Class C+" label retired; cross-references corrected (§0.1.1, §0.1.8, §0.3, §2.2.2, §9.6, §11.3, §14.4, §17.6, §25.6); Annex E severities stated unconditionally; Annex J F9 and F28 dispositions corrected. See Annex Z.

### 0.2 Not adopted (recorded, not silently dropped)

**0.2.1 Internal authority field for UCFS itself (see K12).** The review noted that UCFS uses two levels (normative text and "Design choice" annotations) without marking which is which. v0.3 marks design choices as commentary in §0.1 and removes them from operative clauses. A full internal-authority hierarchy for UCFS is not adopted; the framework treats normative clauses (the MUST/SHOULD body) as level 1 and the §0 changes and annexes as level 2 commentary, but does not apply an internal-authority rule to itself (open item K12).

**0.2.2 Self-application of §24.6 to UCFS itself.** The review recommended a self-application. v0.3 records the recommendation as an open item (§K7). A full self-application would produce a further review; it is not performed here.

**0.2.3 Renaming "Uncertainty Compression" (Red Team suggestion, carried forward from v0.2).** Not adopted. "Compression" is retained as a technical term defined in §3.4, with the note in §3.4 and §3.4.1 that compression is declarative and evidential, not lossy and not permission to suppress or average away uncertainty.

**0.2.4 Fully open-sourcing the harness before the claim model is stable (Red Team suggestion, carried forward from v0.2).** Not adopted. Openness is conditional on a conformance-mark policy (§28.6, Annex I).

### 0.3 Open items carried to Annex K

The following cannot be fixed without information not available to this draft. They are recorded in Annex K, not in operative clauses, so the framework does not appear to answer them:

- **K1:** Whether COLREG provides an equivalence route for Rule 5 (F30).
- **K2:** Whether the ARCVB implementation actually performs the runtime bridge claimed in §24.4.1 (F23).
- **K3:** Whether the class-society notations that §1.8 claims to complement exist in a form the framework can map to (XR1).
- **K4:** Whether an Administration will accept bounded pre-approval of software changes (§18.2, carried forward).
- **K5:** Whether the MASS Code's mandatory timeline (earliest 1 Jan 2032) holds.
- **K6:** Whether a general sensor-sufficiency threshold will be adopted by IMO (§13.2).
- **K7:** A full §24.6 self-application of UCFS to itself.
- **K8:** Whether bounded claims in non-waivable domains should be permitted at all — v0.3 allows them as S2; this is a design choice, not a resolved legal question.
- **K9:** Governance, provenance rules, verification status and confidentiality posture of a shared reference protocol library (§28.7; carried forward from v0.2 §0.4).
- **K10:** Antitrust and confidentiality posture for shared precedent (§28.8; carried forward from v0.2 §0.4).
- **K11:** Insurer and underwriter engagement route (Annex G5; carried forward from v0.2 §0.4).
- **K12:** Internal-authority field for non-hierarchical documents and for UCFS itself (F28; no clause written).

### 0.4 Changes from v0.3 (this version, v0.3.1)

v0.3.1 is a defect-correction release (§28.5.1). It changes annex text, records new open items and watch items, and adds a non-operative proposals annex. No operative clause is added, changed or removed, and no clause number moves, so IAAP v0.2.x and ARCVB v0.1.x references to UCFS clauses remain valid. Findings are from the 15 November 2026 intake of six new documents and `Maritime_Coverage_Gap_Map.md` v2. Every [P] flag below follows §2.2.

| # | Change | Finding or gap that drove it | Clause or register |
|---|---|---|---|
| 0.4.1 | Annex B: Rule 17 rows cite para 61 only (para 60 concerns Rule 16); "observational" and "predictive" marked as the Bridge's reading, not the Court's wording [P] | Bridge corrections A1 | Annex B |
| 0.4.2 | Annex B: steady-bearing row adds paras 98(vi)–(vii) and the observability conditions [P] | Bridge corrections A2 | Annex B; proposal P-6 |
| 0.4.3 | Annex F F2: the 2023 MSC position restated in the qualified form reported by secondary summaries ("remain relevant … no need to amend … at this stage") [P]. The v0.3 wording ("can be applied in full") is recorded here as superseded, not silently overwritten | Bridge corrections A3 (secondary sources only; MSC 107/20 paras 5.48–5.49 unconfirmed) | Annex F F2 |
| 0.4.4 | Annex K: K3 gains the ClassNK datapoint; K12 cites UAIRF v1.1 §7.11 and §12.20 as a model; K13–K23 added | Gap map; ClassNK decks; decisions D3, D5, D6 | Annex K |
| 0.4.5 | Annex H: H11–H13 added | Gap map W2-06, W3-09, W5-03 | Annex H |
| 0.4.6 | Annex E: E7 notes the unexamined MLC 2006 question [P] | Gap map W7-05 | Annex E |
| 0.4.7 | Annex D: "Others" row records a non-binding research priority order | Decision D2 | Annex D |
| 0.4.8 | Annex P added (proposed clauses P-1 to P-6, non-operative, all [P]) | Gap map dispositions (e); Bridge corrections A2, B1 | Annex P |
| 0.4.9 | Annex Z: Z5 records decisions D1(a)–(d), resolved by author delegation on 15 November 2026 | Annex Z "Decisions to confirm" | Annex Z Z5 |
| 0.4.10 | Annex L: L7 lineage declaration for v0.3 → v0.3.1 | UAIRF v1.1 §26.6 | Annex L |

**Contradictions recorded, not overwritten.** (i) v0.3 Annex F F2 against the qualified MSC wording in the corrected Bridge paper (0.4.3). (ii) v0.3 Annex B "paras 60–61" against the corrected Bridge reading of para 61 (0.4.1). (iii) ClassNK slides place navigation systems in UR E26 cyber scope; §20.1 and the Bridge call the cyber-to-COLREG link an inference. These do not conflict (E26 does not mention COLREG), but the qualifier is recorded as open item K22 and §20.1 is not changed.

**Double-count rule.** A watch item (Annex H) converts to a submitter-owned open item on its trigger. H12 converts to K15 and H13 to K17. They are one subject at different stages, not two items.

---

## 1. Scope, purpose and positioning

### 1.1 Purpose

1.1.1 UCFS is a normative framework for converting regulatory, legal, perceptual, operational and evidentiary uncertainty into declared, bounded, testable and auditable claims.

1.1.2 UCFS is the parent specification. ARCVB is its implementation pipeline. The MASS Regulatory Bridge is the friction and evidence source map.

### 1.2 Application

1.2.1 UCFS applies to any maritime autonomous surface ship (MASS), any remote operations centre (ROC), and any approval, verification, audit or conformance activity that claims UCFS conformance.

1.2.2 UCFS applies to IMO autonomy degrees one to four and to mixed-mode voyages.

1.2.3 UCFS applies to the regulatory domains listed in clause 1.3 and to case law governing their interpretation.

### 1.3 Regulatory domains

1.3.1 COLREG, including Parts C, D and F.

1.3.2 SOLAS, including chapters II-1, II-2, III, IV, V, IX, XI-1, XI-2 and XIII.

1.3.3 The ISM Code and the ISPS Code.

1.3.4 MARPOL and its Protocol I.

1.3.5 STCW.

1.3.6 Load Lines and the IS Code.

1.3.7 The MASS Code (MSC.595(111)) as guidance **[P]** — see §2.3.

1.3.8 National law and regulator practice.

1.3.9 Case law that governs these instruments.

### 1.4 Limits

1.4.1 UCFS does not determine legal liability.

1.4.2 UCFS does not replace Administration approval.

1.4.3 UCFS does not create a mandatory regime for ships outside the MASS Code's scope.

1.4.4 UCFS MUST NOT be cited as evidence that a ship complies with any instrument.

### 1.5 Relationship to the MASS Code

1.5.1 Where UCFS uses the word "expects" or "requires" in relation to the MASS Code, it means guidance, not obligation.

1.5.2 UCFS MUST NOT upgrade the MASS Code's status.

### 1.6 Relationship to case law

1.6.1 UCFS treats case law as interpretive authority within its jurisdiction and as persuasive authority only where the governing law of the operating jurisdiction treats foreign case law as persuasive.

1.6.2 A UCFS claim relying on case law MUST state the jurisdiction in which the interpretation governs and whether the submitter elects it as the governing interpretation elsewhere.

### 1.7 Relationship to the Bridge

1.7.1 The Bridge's friction register (§3) seeds the UCFS claim register (Annex A).

1.7.2 The Bridge's verification table (§7.1) seeds the UCFS provisional flag register (Annex A, [P] column).

1.7.3 UCFS MUST NOT upgrade the Bridge's verification status for any source; where the two documents disagree on a source's status, §2.3 governs.

### 1.8 Complementarity with classification-society rules

1.8.1 UCFS is a claim-and-evidence layer, not a rule set. It is intended to map to and complement classification-society notations for autonomy, remote control and digitalization.

1.8.2 UCFS MUST NOT be presented as a classification rule, a notation, or a substitute for class approval.

1.8.3 A conformance claim SHOULD declare the classification notations the vessel holds or seeks.

1.8.4 Where a class notation is more specific than a UCFS clause, the notation governs the technical requirements and UCFS records the claim against it.

1.8.5 The specific mapping between UCFS and any class notation is an open item (Annex K3).

---

## 2. Normative references

### 2.1 Primary references

- Resolution MSC.595(111) (adopted 21 May 2026) **[P]** — see §2.3.
- MSC.1/Circ.1638 (3 June 2021) **[P]**.
- Report of MSC on its 107th session (May 2023), paras 5.48–5.49 **[P — report number to be confirmed]**.
- COLREG, 1972, as amended, including Part F (Rules 39–41) and IMO Assembly resolution A.1085(28).
- SOLAS, MARPOL, STCW, ISM Code, ISPS Code, Load Lines, IS Code (operative texts not re-verified in the Bridge).
- *Evergreen Marine (UK) Ltd v Nautical Challenge Ltd* [2021] UKSC 6 (*Ever Smart*) **[P — holdings and paragraph numbers not re-verified]**.
- *The Pennsylvania*, 86 U.S. (19 Wall.) 125 (1873 term).
- 46 U.S.C. §§ 8101, 8102, 8103, 8301, 8502, 4312; 14 U.S.C. § 501 note (2022 at-sea recovery pilot); 46 C.F.R. §§ 15.715, 62.50; 33 C.F.R. Part 83.
- US Coast Guard Work Instruction 5P-WI-002(1) (1 June 2026).
- US Coast Guard CG-ENG Policy Letter 01-23 (17 March 2023).
- Transport Canada TP 13585.
- UK SI 2023/1216.
- Norwegian Maritime Authority circular RSV 12-2020.
- GAO-22-104567, GAO-24-107059, GAO-26-109014, GAO-26-108762 **[P — testimony seen only in excerpts]**.

### 2.2 Provisional clause rule

2.2.1 A clause marked [P] rests on a source whose verification status is not "verified against primary or official text."

2.2.2 A [P] clause MUST NOT support a conformance claim unless either:

- (a) the submitter verifies the source and records a verification record (the source, the primary or official text consulted, the date, and the result); or
- (b) the approval authority accepts the [P] status in writing and the acceptance is recorded in the approval basis.

2.2.3 A claim register MUST record, per claim, the provisional status of every source it relies on and the route (a) or (b) by which the [P] status was cleared.

### 2.3 Source-status reconciliation

2.3.1 Where the Bridge and UCFS disagree on a source's verification status, the more conservative status governs until the source is verified.

2.3.2 The Bridge marks Resolution MSC.595(111) as verified against official text; UCFS marks it [P] because the operative text was not re-read in preparing UCFS. The submitter MUST reconcile the two in the claim register, recording which verification is relied on.

2.3.3 The Bridge marks *Ever Smart* as "not re-verified for this paper"; UCFS carries [P].

### 2.4 Amendment

2.4.1 Where an instrument is amended, the amended text governs.

2.4.2 UCFS clauses do not fix the text of any instrument.

---

## 3. Terms and definitions

3.1 **ANS** — autonomous navigation system. Performs navigation functions under the master's authority.

3.2 **Approval basis** — the vessel-specific document submitted by the applicant and approved by the Administration on which approval and certification rest.

3.3 **Claim** — a UCFS object asserting how a specific obligation is met, bounded, found inapplicable, left open, or failed, with all attributes in §8.

3.4 **Compression** — the act of reducing an uncertainty from implicit to one of: closed, bounded, not applicable, open residue, or failed. Compression is declarative and evidential, not lossy. It does not discard the uncertainty; it records it, its resolution route, its evidence and its residual risk. It is reversible on a re-open trigger.
3.4.1 Compression MUST NOT be read as permission to suppress or average away uncertainty.

3.5 **Compression operator** — a normative transformation defined in §7.4.

3.6 **Compression type** — the mode by which a claim resolves its uncertainty. The permitted values are: application, interpretation, equivalence, departure, bounded fallback, not applicable, open residue, failed (§8.3). A claim MAY carry a compression type set (two or more) where the resolution genuinely rests on more than one mode; the set is ordered by declared priority (§8.3.9).

3.7 **Status** — the acceptance state of a claim. The permitted values are: closed, bounded, not applicable, open residue, failed (§8.1.1).

3.8 **Status–compression correspondence.** Not every status is a compression type and not every compression type is a status. The mapping is declared in §8.3.10. In summary:

- Closed claims are resolved by application, interpretation, equivalence, or departure.
- Bounded claims are resolved by bounded fallback.
- Not-applicable claims are resolved by the not-applicable compression type.
- Open-residue claims are resolved by open residue.
- Failed claims are resolved by failed.

3.9 **Conformance vector** — the five-dimension measurement in §4.2. A conformance claim is separate (§4.1.1).

3.10 **ConOps** — concept of operations.

3.11 **Decision gate** — a conformance checkpoint in §5.

3.12 **Derivation protocol** — the method by which a threshold, bound, propagation model or confidence band is set, justified and verified (§8.6).

3.13 **E4 obligation** — the post-approval data-collection commitment defined in §8.5.6.

3.14 **Evidence item** — an artifact, test result, record or log supporting a claim, with timing and tier.

3.15 **Evidence tier** — E1 declaration, E2 demonstration, E3 independent verification, E4 operational evidence (§8.5).

3.16 **External watch item** — an uncertainty UCFS cannot close or bound because it is outside the submitter's control (§8.9).

3.17 **MASS** — maritime autonomous surface ship.

3.18 **MASS Record** — the document under the MASS Code containing the regulatory gap analysis **[P]**.

3.19 **Non-waivable domain** — a domain in which an open residue blocks the gate and cannot waive it (§5.4). A bounded claim in a non-waivable domain is S2, not S1 (§5.4.2).

3.20 **OE** — operational envelope.

3.21 **Open residue** — a submitter-owned uncertainty that cannot be closed or bounded on the evidence available at the approval decision, declared with owner, legal route, approval authority and re-open trigger.

3.22 **PNT integrity** — the integrity, availability and authenticity of position, navigation and timing data (§20.2).

3.23 **Regulatory claim register** — the consolidated set of all claims, residues and watch items for a vessel or ROC.

3.24 **Responsibility matrix** — the allocation of every navigational-safety responsibility from flag State to ANS, with no unowned responsibility.

3.25 **ROC** — remote operations centre.

3.26 **Rule-set plurality** — the condition in which international and national inland rules, or different national regimes, apply to different phases or geographies of a voyage.

3.27 **Runtime claim validity** — the requirement that a closed or bounded claim remains true during operation, monitored at runtime (§24).

3.28 **Sensor-sufficiency threshold** — the declared minimum data confidence below which the ANS MUST alert the master and enter a declared degraded or fallback state.

3.29 **Severity class** — S1 (blocking), S2 (bounding), S3 (monitoring) per §8.8.

3.30 **Sub-item** — a declared subdivision of a domain for the purpose of assigning evidence-tier minimums (§6.4.1, §6.4.2, §8.5.5).

3.31 **Time architecture** — the declared time source(s), synchronization, drift bounds, holdover and integrity monitoring used by the audit ledger (§26.5).

3.32 **Uncertainty floor** — the declared minimum accuracy or confidence below which a claim's observable is treated as insufficient.

3.33 **Version lock** — the declared instrument, case-law, class-notation and software versions against which a claim is proved.

3.34 **Re-open trigger** — a defined change event that invalidates a claim.

3.35 **Closed** — resolved by a declared, testable claim whose evidence exists at or before the approval decision.

3.36 **Bounded** — controlled by an approved threshold, fallback state, hysteresis, escalation route and owner, with defined re-open conditions.

3.37 **Failed / operation not permitted** — the claim cannot be satisfied at the declared evidence tier or in a non-waivable domain. The operation is not permitted until the claim is closed, or the operation is outside UCFS scope.

---

## 4. Conformance

### 4.1 Conformance principle

4.1.1 A system, approval package or audit MAY claim UCFS conformance only if:

- (a) it states its conformance vector (a measurement, §4.2);
- (b) it satisfies the gates (§5) at the level required by its declared vector; and
- (c) it satisfies every MUST clause applicable to its declared vector.

4.1.2 A conformance claim MUST state the vessel or ROC identifier, jurisdiction, version lock, and the vector.

4.1.3 Conformance is a separate claim from the vector. The vector measures what the system has; conformance asserts that the gates and applicable MUSTs are satisfied at that measurement.

### 4.2 Conformance vector (measurement)

4.2.1 The vector is a measurement of five dimensions. Each dimension has a level 0–3.

| Dimension | L0 | L1 | L2 | L3 |
|---|---|---|---|---|
| **C** — Claim completeness | No register | Some frictions mapped | All in-scope frictions mapped to a claim, N/A, residue or watch item | Full register with cross-links and consistency check |
| **B** — Boundedness | No thresholds | Some thresholds | All bounded claims carry threshold, fallback, hysteresis, escalation, owner, re-open trigger | Plus severity classes and non-waivable list applied |
| **V** — Verification | No test | Some scenarios | V&V harness executes all closed and bounded claims | Plus independent review or E3 evidence for high-tier claims |
| **E** — Evidence | Declarations only | Some E2 | Evidence tiers declared per claim; minimum tiers met | Plus retention, custody, access, privilege and time architecture |
| **P** — Package consistency | Documents disagree | Partial consistency | Approval Basis, ConOps, Responsibility Matrix and Gap Analysis generated as views over the register | Plus drift triggers, certificate register and PSC interface |

4.2.2 A vector is stated as a tuple, e.g., C3-B2-V2-E2-P2.

4.2.3 A conformance claim MUST NOT assert a level higher than the measurement supports.

4.2.4 Dimensions are not fully orthogonal. The C3 consistency check and the P3 drift triggers both involve consistency; the B3 severity classes and the V3 evidence minimums both depend on the claim model. The vector measures five related dimensions; a level in one does not imply or exclude a level in another, but the dimensions are not mathematically independent. This is acknowledged, not concealed.

### 4.3 Minimum vectors by audience

4.3.1 Small operators (Annex G) MAY measure a vector of C2-B1-V0-E1-P1 for early-stage engagement, but MUST NOT operate outside a declared trial or exemption regime.

4.3.2 Approval package MUST achieve C3-B3-V2-E3-P3 and satisfy all gates at the levels required by §5.

4.3.3 Fleet operator SHOULD achieve C3-B3-V3-E3-P3 including fleet-level claims.

4.3.4 An Administration MAY set higher minimums. It MUST NOT accept lower minimums than those needed to satisfy §5.4.

---

## 5. Decision gates and severity

### 5.1 Gate sequence

5.1.1 The following gates MUST be satisfied in order.

- **G0** — Scope and jurisdiction locked.
- **G1** — Claim register complete.
- **G2** — Rule-switching, sensor sufficiency and runtime monitors verified.
- **G3** — Responsibility and statutory complement resolved.
- **G4** — Drift and change control locked.
- **G5** — Evidence, ledger, time architecture and privilege retained.
- **G6** — Approval package consistent, with V&V results included.

### 5.2 Gate requirements

5.2.1 A gate is passed only if every S1 residue in scope is closed and every S2 residue is bounded with owner, fallback and re-open trigger.

5.2.2 An S3 residue MAY remain open at any gate, with monitoring.

5.2.3 A gate MUST record its pass/fail decision, the residues in scope and their severity classes, in the audit ledger.

5.2.4 **G2 requires runtime monitor evidence.** At G2, the runtime monitors required by §24 for every closed and bounded claim in scope MUST be specified, and their test evidence (at least E2) MUST be present. A claim without a specified, tested runtime monitor cannot close at G2.

5.2.5 **G6 requires V&V results.** At G6, the V&V results for every closed and bounded claim MUST be present in the package, with evidence tier and artifact reference.

### 5.3 Gate waiver

5.3.1 A gate MAY be waived only by an S2 or S3 residue in a waivable domain, recorded with the waiver authority and the re-open trigger.

5.3.2 A gate MUST NOT be waived by an S1 residue or by any residue in a non-waivable domain.

### 5.4 Non-waivable domains (fixed minimum list)

5.4.1 The following are non-waivable. An Administration MAY add; it MUST NOT subtract.

| Ref | Non-waivable domain | Rationale |
|---|---|---|
| NW-1 | Rule 5 look-out (application / interpretation, not equivalence) (D-C) | The Bridge's sharpest friction; USCG has stated COLREG compliance for autonomous look-out is not established. |
| NW-2 | Rule 17(b) prediction (D-D) | Mandatory stand-on action; prediction error is a collision-causation route. |
| NW-3 | Statutory complement (D-F) | Statutes cannot be waived by approval; a MASS approvable under the Code may still need the statutory complement. |
| NW-4 | MARPOL Annex I (D-G) | Oil pollution obligations; unmanned machinery spaces. |
| NW-5 | ISM and ISPS interfaces (D-G) | The ISM quadrilateral and the ROC security plan are load-bearing for responsibility. |
| NW-6 | Responsibility matrix completeness (D-F) | No unowned responsibility at any handover boundary. |
| NW-7 | Time architecture and tamper-evidence (D-H) | Without these, the ledger is not evidence. |
| NW-8 | Change-control classification (D-I) | A version-locked approval basis without classification is not approvable. |

5.4.2 **Residues vs bounded claims in non-waivable domains.**

- A residue in a non-waivable domain is S1 and MUST block the gate.
- A bounded claim in a non-waivable domain is S2 and MUST carry a runtime monitor that escalates to the master on threshold breach (§8.10.3). A bounded claim is not a residue.

5.4.3 **Off-list non-waivable domains.** The submitter MUST identify any non-waivable domain under the flag State's law not listed in this section and MUST record it in the claim register as an S1 domain for the purposes of this framework.

### 5.5 Gate integrity rule

5.5.1 A gate passed in violation of §5.3 or §5.4 is void and MUST be recorded as a conformance failure.

5.5.2 The audit ledger MUST flag a void gate.

---

## 6. Uncertainty taxonomy

### 6.1 Requirement

6.1.1 Every uncertainty in scope MUST be assigned to exactly one domain in §6.3.

6.1.2 Where an uncertainty spans domains, it MUST be split into one claim per domain, linked by a shared obligation reference.

### 6.2 Assignment record

6.2.1 Domain assignment MUST be recorded in the claim register and reflected in Annex A.

### 6.3 Domains

| Ref | Domain | Scope |
|---|---|---|
| D-A | Legal-textual and jurisdictional | Rule text, governing interpretation, flag/coastal/port law, statutory complement |
| D-B | Case-law interpretive | *Ever Smart*, *Pennsylvania*, national appellate formulations |
| D-C | Perceptual and sensor-sufficiency | Rule 5 look-out, scanty information, restricted visibility, fused sensing |
| D-D | Predictive | Rules 6, 7, 8, 17(b); CPA/TCPA; decision latency |
| D-E | Operational and handover | Detection-to-intervention, authority transfer, SA rebuild, ROC workload, alarm load |
| D-F | Responsibility and statutory complement | Flag State, Company, ship, ROC, master, ANS; statutory manning |
| D-G | Environmental and safety instrument | SOLAS chapters, MARPOL annexes, ISM, ISPS, Load Lines, IS Code |
| D-H | Documentary and evidentiary | Acceptance criteria, evidence timing, tiers, retention, custody, access, privilege, time |
| D-I | Version and drift | Software cadence, treaty amendments, case-law change, class-notation change |
| D-J | Scope and application gate | MASS Code application, small MASS, exclusions |
| D-K | Cyber, PNT and non-cooperative | Cyber-induced degraded states, PNT integrity, deceptive or poorly detectable targets |
| D-L | Liability and investigative evidence | *Pennsylvania*, causation, investigator usability |
| D-M | Communications | SOLAS IV, GMDSS, VHF watch, bridge-to-bridge, distress alerting |
| D-N | Practical seamanship | Pilotage embarkation, anchoring, mooring, SAR coordination, medical care, salvage and towage, tug and escort |

### 6.4 Domain sub-items (declared)

6.4.1 **D-C sub-items:**

- D-C.1 — Rule 5 look-out (equivalence or application).
- D-C.2 — Degraded states and sensor-sufficiency threshold.
- D-C.3 — Rule 7(c) scanty information.
- D-C.4 — Rule 19 restricted visibility.
- D-C.5 — Parts C and D lights, shapes and signals.

6.4.2 **D-D sub-items:**

- D-D.1 — Rule 6 safe speed.
- D-D.2 — Rule 8 avoiding action (magnitude and timing).
- D-D.3 — Rule 17(b) prediction.
- D-D.4 — Decision latency.

6.4.3 The sub-items are the referents for the evidence-tier minimum table in §8.5.5. They do not change the domain assignment of §6.1.

### 6.5 Reclassification

6.5.1 A domain assignment MAY be changed only by a recorded amendment in the claim register, with the reason and re-assessment.

6.5.2 A reclassification MUST trigger a consistency check (§9.6).

---

## 7. Compression operators

### 7.1 Operator list (expanded from v0.1)

- **APPLY** — the obligation is satisfied by non-human means without the rule being read as altered (default for Rule 5 under clause 10.1).
- **INTERPRET** — declare the governing interpretation of a contested text and the jurisdiction in which it governs.
- **ASSIGN-JURISDICTION** — assign flag, coastal, port or inland rule and the legal route.
- **ENCODE-OBSERVABLE** — translate a legal test into measurable observables.
- **THRESHOLD** — set a numeric or logical bound with derivation protocol.
- **BOUND** — declare fallback, hysteresis, escalation route and owner.
- **ESCALATE** — declare the trigger and route by which the ANS hands authority to the master or ROC.
- **OWN** — assign an owner to the claim and to any unowned role.
- **VERSION-LOCK** — record instrument, case-law, class-notation and software versions.
- **RETAIN** — declare retention, custody, access, integrity and privilege arrangements.
- **DECLARE-OPEN** — record a submitter-owned residue with owner, route, authority and re-open trigger.
- **DECLARE-WATCH** — record an external watch item with monitoring owner and trigger.
- **DECLARE-NA** — record a not-applicable finding with justification and owner.
- **FAIL** — record a failed claim and the operation-not-permitted consequence.
- **DERIVE** — apply the derivation protocol to a threshold (clause 8.6).
- **PROPAGATE** — apply the uncertainty propagation model to derived observables (clause 9.5).
- **CONSISTENCY-CHECK** — test mutual satisfiability with linked claims (clause 9.6).

### 7.2 Operator discipline

7.2.1 An operator MUST NOT be applied in a way that alters the text of an instrument.

7.2.2 APPLY and INTERPRET stay within the rule.

7.2.3 A departure MUST be tagged as a departure (clause 8.3.4) and handled under clause 8.7.

### 7.4 Operator list

APPLY, INTERPRET, ASSIGN-JURISDICTION, ENCODE-OBSERVABLE, THRESHOLD, DERIVE, BOUND, ESCALATE, OWN, VERSION-LOCK, RETAIN, DECLARE-OPEN, DECLARE-WATCH, DECLARE-NA, FAIL, PROPAGATE, CONSISTENCY-CHECK — as defined in v0.2 §7.1.

---

## 8. The Regulatory Claim model (revised)

### 8.1 Claim status (five values)

8.1.1 Every claim MUST have exactly one status: closed, bounded, not applicable, open residue, or failed.

8.1.2 Failed means the claim cannot be satisfied at the declared evidence tier or in a non-waivable domain. A failed claim triggers the operation-not-permitted consequence in clause 8.1.3.

8.1.3 A failed claim in a non-waivable domain MUST suspend the approval or operation until the claim is closed.

8.1.4 A failed claim in a waivable domain MAY be converted to a bounded claim if a bounded fallback satisfying clause 8.10 exists. The conversion changes both the compression type (to "bounded fallback") and the status (to "bounded"), and MUST be recorded as a conversion event in the ledger.

### 8.2 Claim attributes

8.2.1 Every claim MUST carry the following attributes:

- claim identifier;
- obligation reference;
- domain (§6.3);
- sub-item, where applicable (§6.4);
- jurisdiction;
- compression type set (§8.3) — one or more values, ordered by priority;
- status (§8.1.1);
- evidence tier minimum (§8.5);
- contestation level (§8.11);
- confidence band and its derivation protocol (§8.11);
- observable;
- threshold or bound;
- derivation protocol reference (§8.6);
- uncertainty propagation reference (§9.5);
- acceptance criterion;
- evidence item(s) and timing relative to the approval decision;
- owner;
- version lock;
- failure mode and response (§8.4) — exempt for N/A claims per §8.4.3;
- runtime monitor (§24);
- re-open trigger;
- severity class (§8.8).

8.2.2 A claim lacking any required attribute MUST NOT be recorded as closed or bounded.

### 8.3 Compression types (eight values, settable)

8.3.1 **Application** — the obligation is satisfied by non-human means without the rule being read as altered. MUST NOT be used where the instrument provides a formal equivalence route and the submitter is relying on it.

8.3.2 **Interpretation** — the obligation's terms are read a particular way. MUST state the jurisdiction whose interpretation is relied on.

8.3.3 **Equivalence** — a formal alternative under an instrument's equivalence provision. MUST identify the provision (for example SOLAS) and MUST NOT be applied to COLREG unless the framework's open item K1 is resolved in favour of a COLREG equivalence route.

8.3.4 **Departure** — a departure from a mandatory legacy provision. MUST identify the provision, the flag-State authority relied on, and the risk assessment.

8.3.5 **Bounded fallback** — the claim is bounded (§8.10).

8.3.6 **Not applicable** — the obligation does not engage; justification and owner required.

8.3.7 **Open residue** — a submitter-owned residue (§8.8).

8.3.8 **Failed** — the claim cannot be satisfied at the required tier or in a non-waivable domain.

8.3.9 **Compression type set.** A claim MAY carry more than one compression type when the resolution genuinely rests on more than one mode. Example: a Rule 5 claim may be [application, interpretation] — the machine look-out satisfies the rule (application) and "sight and hearing" is read as including fused sensing (interpretation). The set MUST be ordered by declared priority and MUST state which type governs if the two would conflict.

8.3.10 **Mapping between compression type and status.** The following mapping is normative:

| Status | Permitted compression type(s) |
|---|---|
| Closed | application, interpretation, equivalence, departure, or a set of these |
| Bounded | bounded fallback |
| Not applicable | not applicable |
| Open residue | open residue |
| Failed | failed |

A claim with a compression type not permitted for its status MUST NOT be recorded as that status.


### 8.4 Failure modes

8.4.1 Every closed or bounded claim MUST declare its failure mode(s), detection method, response and responsible actor.

8.4.2 A claim without a declared failure mode MUST be recorded as bounded, not closed.

8.4.3 N/A claims are exempt from the failure-mode requirement. In place of a failure mode, an N/A claim MUST declare its reverse-evidence trigger: the observation that would convert it from N/A to an active claim.

### 8.5 Evidence tiers

8.5.1 **E1 — Declaration.** A signed statement by the submitter.

8.5.2 **E2 — Demonstration.** Test, simulation, bench trial or sea trial result produced by the submitter or the developer.

8.5.3 **E3 — Independent verification.** Verification by an Administration, recognized organization, classification society, or an accredited third party independent of the developer.

8.5.4 **E4 — Operational evidence.** Service history, continuing reliability data, incident and near-miss data, and maintenance records from actual operation.

8.5.5 **Minimum tiers by domain and sub-item.**

| Domain / sub-item | Minimum for closure | Minimum for bounded |
|---|---|---|
| D-A | E1 | E1 |
| D-B | E1 | E1 |
| D-C.1 (Rule 5 look-out) | E3 | E2 + E4 obligation |
| D-C.2 (degraded states) | E2 | E2 + E4 obligation |
| D-C.3 (Rule 7(c)) | E2 | E2 |
| D-C.4 (Rule 19) | E2 | E2 |
| D-C.5 (Parts C/D) | E2 | E2 |
| D-D.1 (Rule 6) | E2 | E2 |
| D-D.2 (Rule 8) | E2 | E2 |
| D-D.3 (Rule 17(b)) | E3 | E2 + E4 obligation |
| D-D.4 (decision latency) | E2 | E2 |
| D-E | E2 | E2 + E4 obligation |
| D-F (matrix) | E1 | E1 |
| D-F (statutory complement route) | E2 | E1 |
| D-G | E2 | E1 + E4 obligation |
| D-H | E2 | E1 |
| D-I | E1 | E1 |
| D-J | E1 | E1 |
| D-K | E2 | E2 |
| D-L | E1 | E1 |
| D-M | E2 | E1 |
| D-N | E2 | E1 |

8.5.6 **E4 obligation defined.** Where a bounded claim requires "E4 obligation," the submitter MUST declare:

- (a) the data-collection plan (what data, from what operations, at what cadence);
- (b) the reporting cadence to the Administration;
- (c) the re-assessment trigger (e.g., an incident, a threshold breach, a defined sample size reached);
- (d) the declared fallback if E4 evidence does not materialize within a declared period (e.g., continued bounded operation with enhanced monitoring, or suspension);
- (e) the owner of the E4 obligation.

8.5.7 An Administration MAY raise a minimum tier. It MUST NOT lower the tiers for NW-1, NW-2, NW-3, NW-4 or NW-5.

### 8.6 Derivation protocol

8.6.1 Every threshold claim MUST carry a derivation protocol including:

- target set definition (size, signature class, aspect, range);
- environmental matrix (visibility, sea state, clutter, background light);
- metric and pass condition;
- calibration and reference evidence;
- sensitivity analysis around the chosen threshold;
- independent review route;
- declared sensitivity band within which the threshold may move without re-approval.

8.6.2 Where no accepted benchmark exists, the claim MUST carry a method justification stating why the chosen method is fit for purpose, and a sensitivity band.

8.6.3 A threshold declared without a derivation protocol MUST NOT close the claim.

8.6.4 The derivation protocol is referenced by identifier in the claim register.

8.6.5 The derivation protocol is required for thresholds, uncertainty propagation models (§9.5), confidence bands (§8.11.5), and the Rule 19 fusion state (§12.6.2).

### 8.7 Interpretation versus departure

8.7.1 A claim tagged as interpretation MUST NOT be used to justify a departure from the text.

8.7.2 A departure claim MUST identify the mandatory legacy provision, the flag-State authority, and the risk assessment.

8.7.3 A departure claim MUST remain subject to the mandatory legacy provision until the flag State accepts it.

### 8.8 Open residues and severity classes

8.8.1 An open residue MUST declare: the question; why it cannot be closed or bounded on available evidence; the owner; the legal route relied on pending resolution; the approval authority that accepted it; and the re-open trigger.

8.8.2 Severity classes:

- **S1 — Blocking.** The residue is in a non-waivable domain. Blocks the gate. Cannot be waived.
- **S2 — Bounding.** The residue is in a waivable domain but is bounded by a declared fallback with owner, escalation and re-open trigger. Permits the gate but constrains operation.
- **S3 — Monitoring.** The residue is monitored at runtime and does not constrain operation unless its trigger fires.

8.8.3 **Severity assignment rule** (single formulation, replacing the two v0.2 formulations):

- A residue in a non-waivable domain is S1.
- A residue in a waivable domain is S2 or S3, according to the submitter's justification.
- A bounded claim in a non-waivable domain is S2 with a runtime escalation obligation (§8.10.3); the bounded claim is not a residue, so the S1 rule for residues does not apply.

8.8.4 The severity class MUST be recorded in the audit ledger and reviewed at every gate.

### 8.9 External watch items

8.9.1 An external watch item is an uncertainty outside the submitter's control. It MUST declare: the question; the external actor(s) whose action would resolve it; the monitoring owner; the monitoring method; and the trigger that converts it into a submitter-owned residue.

8.9.2 Watch items MUST NOT be presented as satisfying any obligation.

8.9.3 Watch items are recorded in Annex H.

### 8.10 Bounded claims

8.10.1 A bounded claim MUST declare: threshold; fallback state; hysteresis; escalation route; owner; runtime monitor; severity class; re-open trigger.

8.10.2 A bounded claim without a fallback state MUST NOT be approved as bounded.

8.10.3 A bounded claim in a non-waivable domain MUST carry S2 severity and a runtime monitor that escalates to the master on threshold breach. The runtime monitor is a gate requirement at G2 (§5.2.4).

### 8.11 Contestation and confidence

8.11.1 Every claim MUST carry a contestation level: settled, persuasive, contested, or novel.

8.11.2 Every claim MUST carry a confidence band: the range within which the claim's observable is expected to remain without re-assessment.

8.11.3 A novel or contested claim MUST be flagged in the approval basis and MUST NOT be represented to an Administration as settled.

8.11.4 A confidence band breach is a re-open trigger.

8.11.5 The confidence band MUST carry a derivation protocol (§8.6). The protocol must state the method (statistical, empirical, or judgment-based), the sample or basis, and the sensitivity of the band to the method chosen.

---

## 9. Compression rules (invariants)

9.1 **No unowned uncertainty.** Every claim, residue and watch item has an owner. Every responsibility in the matrix has an owner.

9.2 **No unbounded threshold.** Every threshold has a bound, derivation protocol and acceptance criterion.

9.3 **No evidence without timing or tier.** Every evidence item states when it will exist and its tier.

9.4 **No rule switch without observables and hysteresis.**

9.5 **Uncertainty propagation.** Every observable derived from a measurement (bearing rate, CPA, TCPA, closure rate, range) MUST carry an uncertainty propagation model with declared confidence intervals. The effect on rule engagement and on Rule 17(b) MUST be stated.

9.5.1 The uncertainty propagation model MUST carry a derivation protocol (§8.6). The protocol must state the propagation method (e.g., interval arithmetic, Kalman covariance, Monte Carlo with declared sample size), the assumptions, and the sensitivity of the propagated uncertainty to the method chosen.

9.6 **Consistency.** Claims sharing an obligation reference or a runtime resource (time, sensor, operator attention) MUST be checked for mutual satisfiability at every gate. A conflict is an open residue; its severity class is assigned under clause 8.8.3.

9.7 **No handover without latency budget and authority record.**

9.8 **No statutory complement ignored.** The legal route — statutory change, pilot authority, exemption, equivalence, or none — MUST be declared.

9.9 **No MARPOL annex omitted.** Annex-by-annex declaration is required (Annex C).

9.10 **No version without drift trigger.**

9.11 **Interpretation and departure are tagged separately.**

9.12 **No audit claim without retention, access, integrity and privilege arrangements.**

9.13 **No claim may upgrade a source's verification status.**

9.14 **No subsystem may override a claim.** A subsystem that detects a condition inconsistent with a closed or bounded claim MUST raise an escalation event, record it in the audit ledger, and re-open the claim.

9.15 **No failed claim may be converted to closed without new evidence at the required tier.**

9.16 **No gate may be passed with an S1 residue.**

---

## 10. Domain D-A — Legal-textual and jurisdictional

10.1 Governing interpretation per contested rule (operator INTERPRET).

10.2 **Application gate:** the approval basis MUST record the Administration's impracticability/insufficiency decision, the instruments found insufficient and the chapters invoked. The gate is an S2 claim with an owner and a re-open trigger.

10.3 **Scope decision:** the approval basis MUST state whether the vessel is within the MASS Code's scope (cargo ships ≥ 500 GT to which SOLAS applies), outside it, or within the invitation to apply below 500 GT.

10.4 **Exclusions:** cargo high-speed craft (SOLAS X), warships, naval auxiliaries and other government non-commercial ships MUST be recorded where relevant.

10.5 **Degrees of autonomy and mixed-mode transitions:** the register MUST record degrees and transitions.

10.6 **Rule-set plurality:** where the voyage crosses a demarcation between international and inland rules, the register MUST declare the rule set by phase and geography; V&V MUST test the transition.

10.7 **Small MASS:** MUST declare national small-vessel measures relied on and MUST NOT assume the MASS Code applies.

10.8 **Interpretation vs departure** (operator discipline per clause 8.7).

---

## 11. Domain D-B — Case-law interpretive

11.1 ***Ever Smart* scoping.** Claims relying on *Ever Smart* MUST state that the holdings are UK law and MUST state the governing interpretation relied on in the vessel's operating jurisdiction. Where *Ever Smart* is not binding, the submitter MUST elect it as the governing interpretation or state what is relied on instead.

11.1.1 The claim that *Ever Smart* is "persuasive elsewhere" is narrowed. The claim is: "the holdings are persuasive in common-law jurisdictions that treat foreign case law as persuasive; their status in other jurisdictions is determined by the governing law." The narrower claim is **[P]** and MUST be verified for each operating jurisdiction before a conformance claim relies on it.

11.2 **Steady bearing.** A crossing-rule engagement claim MUST NOT require a steady course as a precondition. It MUST declare bearing-rate measurement accuracy and the observables used to detect a steady bearing.

11.3 **Shaping to enter.** A rule-switching claim MUST declare observable criteria for shaping to enter (course adjustment, alignment with the entrance on the starboard side, final approach), the states, transitions, reversion hysteresis and verification scenarios (clause 25).

11.4 A vessel already aligned and closing without a detectable course adjustment MUST be addressed by the claim, either as a declared design question or as a bounded fallback.

11.5 **Rule 17 triggers.** Separate claims are REQUIRED for 17(a)(ii) (observational) and 17(b) (predictive).

11.6 **Timing and legibility.** The register MUST declare maximum decision latency and the range and timing at which avoiding action begins. A claim permitting late decisions MUST NOT be approved as satisfying the legibility test.

11.7 **Pennsylvania and causation.** The register MUST record the *Pennsylvania* doctrine, later appellate formulations, and that application to autonomous look-out is a question for counsel.

11.8 **Limits of case-law claims.** The Bridge's Appendix A parameters MUST NOT be cited as a standard or as validated by any Administration or classification society.

---

## 12. Domain D-C — Perceptual and sensor-sufficiency

12.1 **Rule 5 default compression type.** Rule 5 machine look-out defaults to the compression type set [application, interpretation], ordered application-first. A submitter MAY adopt equivalence only by explicitly identifying a formal COLREG equivalence route, which UCFS does not assume exists (see open item K1).

12.1.1 The dual compression type set is permitted under §8.3.9. The set's priority governs if the two would conflict: application governs the question "does the machine look-out satisfy the rule?"; interpretation governs the question "how is 'sight and hearing' read?"

12.2 **Rule 5 claim.** MUST declare the sensor suite and degradation modes; MUST map functions to the Rule's elements (fusion for sight, acoustic for hearing, data links and other sources for "all available means"); MUST demonstrate the mapping in the regulatory gap analysis including performance against small, low-signature targets (target set defined in the derivation protocol); MUST NOT state or imply the Rule's text has changed.

12.3 **Sensor-sufficiency threshold and uncertainty floor.** MUST declare a threshold and a floor with a derivation protocol (clause 8.6). Below the threshold the ANS MUST alert the master and enter a declared degraded or fallback state. The claim MUST state whether the threshold is vessel-specific or relies on a published benchmark, and MUST record that no accepted reference test was identified where that is so.

12.4 **Degraded states.** MUST declare triggers, fallback behaviour and escalation route. MUST be tested by the harness.

12.5 **Rule 7(c) scanty information.** MUST declare the sensor-sufficiency threshold and uncertainty floor for Rule 7(c). MUST state that "scanty" has no sensor-data threshold in the Code.


12.6 **Rule 19 restricted visibility.** MUST declare the restricted-visibility mode, sensor assumptions, speed policy and prohibited manoeuvres.

12.6.1 MUST define the fusion state treated as equivalent to "detects by radar alone."

12.6.2 The fusion state MUST carry a derivation protocol (§8.6). The protocol must state which sensors are active, which are fused, and how the state corresponds to the Rule's "radar alone" concept.

12.7 **Parts C and D.** MUST provide a survey and verification checklist for lights, shapes and signals, addressing: automated sound-signal activation on restricted visibility; timing, direction and fault detection of signals; manual or remote override; and survey method for Parts C and D. MUST declare who or what activates sound signals on a crewless ship. MUST NOT rely on any unverified national measure without recording its verification status.

12.8 **Look-out evidence.** MUST be retained in investigator-usable form, with the threshold, floor, degradation tests and target set.

---

## 13. Domain D-D — Predictive

13.1 **Rule 6.** MUST express Rule 6 factors as monitored OE parameters with margins. MUST define degraded-state buffers before the OE boundary. MUST state that an OE is a boundary and Rule 6 is a continuous judgment, and MUST declare how the gap is bounded.

13.2 **Rule 7(c).** MUST declare the sensor-sufficiency threshold below which the ANS alerts the master and enters degraded or fallback state. MUST state whether IMO will adopt a general threshold is unknown.

13.3 **Rule 8.** MUST declare manoeuvre magnitude ("large enough") and timing criteria. MUST validate legibility to human visual and radar observers and, separately, to other MASS sensors using a declared peer set and protocol. MUST declare maximum decision latency and range/timing of avoiding action. MUST state that digital signalling supplements but does not replace physical signals and legibility.

13.4 **Rule 17(b).** MUST declare prediction-accuracy requirement, error tolerances, CPA/TCPA criteria and escalation to the master. MUST record that different implementations will set different thresholds and that the approval basis bounds the variation.

13.5 **Decision latency.** A bounded claim with an owner, a derivation protocol and a runtime monitor.

13.6 **Uncertainty propagation.** Bearing rate, CPA, TCPA and closure rate MUST be carried with propagated uncertainty. Rule engagement and 17(b) triggers MUST be stated against the confidence interval, not a point estimate.

13.6.1 The propagation model MUST carry a derivation protocol (§9.5.1).

---

## 14–23. Domains D-E through D-N

### 14. Domain D-E — Operational and handover

14.1 **Detection-to-intervention.** MUST define the event chain: detection → alert → operator acknowledge → SA established → authority accepted → action. MUST declare evidence per segment. MUST declare the ANS fallback behaviour during the chain. MUST declare maximum end-to-end latency.

14.2 **Situation-awareness rebuild.** MUST declare the operator's SA-rebuild time after handover, with evidence, and MUST treat it as a latency component.

14.3 **Rule 2(b).** MUST treat the limits of the ANS, sensors and control link as Rule 2(b) limitations. Human-system limitation analysis supplements and does not replace Rule 2(b). MUST state the Code specifies no maximum latency.

14.4 **Handover record.** The ledger MUST record exact handover timestamps, the authority transfer and the accepting actor, with time-architecture reference (clause 26.5).

14.5 **ROC workload and rest hours.** MUST declare rest-hour records, workload limits, multi-ship alarm-load assessment and the basis for treating remote experience as equivalent to sea service. MUST state that ROC rest-hour and workload implementation is unquantified in the Code and MUST declare vessel-specific quantification. MUST address one master or ROC covering several ships, bounding workload and common-cause risk.

14.6 **Training and qualification.** MUST declare the basis for STCW-not-less qualification, the basis for treating the ROC as directly associated with the bridge, and the basis for remote experience as sea service.

14.7 **Human factors.** MUST address complacency, mode confusion, authority-transfer error and trust calibration, with evidence.

14.8 **Fleet-level claims.** Where one ROC or one master covers multiple ships, fleet-level claims MUST be recorded, with common-cause analysis and a fleet runtime monitor.

14.9 **Responsibility matrix.** The approval basis MUST contain a matrix from flag State to ANS. MUST cover the ISM quadrilateral (Company, ship, ROC, master). MUST identify any responsibility transferred from the ship security officer. MUST NOT leave a responsibility unowned. MUST declare the limits of ANS authority. MUST record that the ANS is not a legal person.

### 15. Domain D-F — Responsibility and statutory complement

15.1 **Statutory complement.** The register MUST declare the statutory complement per mode, how statutory roles (including master) are met, and the legal route relied on: statutory change, pilot authority, exemption, equivalence, or none. MUST NOT assume labour savings statutes do not permit. MUST state the Code's equivalence test is an approval criterion and does not amend a statute.

15.2 **United States.** Claims MUST address 46 U.S.C. §§ 8101, 8102, 8103, 8301, 8502, 4312 as applicable, and the 2022 at-sea recovery pilot. MUST state the Coast Guard's position that it cannot waive the statutes outside the narrow pilot authority. MUST address the 1 June 2026 work instruction as informative (SHOULD), including the requirement not to set manning below the statutory minimum and the request for a ConOps and COLREGS compliance statement. MUST state the work instruction is non-binding by its own terms and that the Code does not directly apply to the unmanned systems it covers. MAY rely on 46 C.F.R. § 15.715 as an analogy for staged approval; MUST NOT present it as a substitute for Code approval.

15.3 **Other jurisdictions.** Canada (TP 13585, technical review board); United Kingdom (SI 2023/1216; exemptions and equivalences for larger ships); Norway (RSV 12-2020; IMO equivalence process). MUST state the surveyed jurisdictions are not exhaustive.

15.4 **Staged approval.** A staged approval MAY be adopted, based on demonstrated and continuing reliability and a planned maintenance programme. The continuously attended mode required until reliability is proven MUST be declared.

15.5 Responsibility matrix completeness (NW-6) is non-waivable.

### 16. Domain D-G — Environmental and safety instruments

16.1 **SOLAS V/19, V/20.** MUST declare how each requirement is met electronically, the chart back-up, V/20 applicability to all MASS, and logged-data availability to the Administration and investigators.

16.2 **SOLAS II-1.** MUST declare the monitoring and alerting function and the human or remote response chain.

16.3 **SOLAS II-2.** MUST declare automated detection, remote or autonomous extinction, external-responder interface, single-compartment fire control and fallback logic.

16.4 **SOLAS III and V/33.** MUST declare crewless deployment, accommodation for rescued persons and their communication with the ROC.

16.5 **SOLAS IV (new).** MUST address GMDSS obligations in a crewless or reduced-crew configuration: distress alerting, watchkeeping, and shore maintenance arrangements. See also D-M.

16.6 **SOLAS XI-2 / ISPS.** MUST extend the ship security plan to the ROC. MUST NOT assume remote operators automatically replace the ship security officer.

16.7 **SOLAS IX / ISM.** MUST use the ship's SMS with a ROC SMS; MUST define interfaces among Company, ship, ROC and master.

16.8 **MARPOL.** Annex-by-annex declaration required (Annex C). MUST state IMO has started scoping work on MARPOL-side instruments and no output was identified when the Bridge was prepared.

16.9 **Load Lines and IS Code.** Compliance mapping and verification in stability and certification documentation.

16.10 **Amendment drift.** Register MUST name the version of each instrument relied on and maintain a table of adopted, accepted, in-force and applicable amendments with defined triggers.

16.11 **Layers of verification.** MUST treat as distinct and cumulative: (1) flag-State implementation audit under the III Code; (2) COLREG Part F audit; (3) casualty investigation under SOLAS XI-1/6; (4) vessel and ROC survey and approval under the Code. MUST NOT collapse the layers.

### 17. Domain D-H — Documentary and evidentiary

17.1 **Acceptance criteria.** Each threshold MUST carry an acceptance criterion stating the test, pass condition and evidence item.

17.2 **Evidence timing.** Each evidence item MUST state whether it exists at the approval decision or will exist after, and the gate at which it will exist.

17.3 **Evidence tier.** Each evidence item MUST state its tier (E1–E4) and MUST meet the domain minimum (clause 8.5.5).

17.4 **Retention.** Retention and access arrangements MUST be declared for look-out evidence, verification results, PNT and time records, and data logs. MUST be investigator-usable.

17.5 **Verification status.** Each source MUST carry its status: verified against primary or official text; verified as a target only; partly verified; not re-verified; not verified. Claims MUST NOT upgrade status.

17.6 **Artifact identity.** Evidence artifacts MUST carry type, producer, timestamp (per time architecture, clause 26.5), integrity method and custody history.

17.7 **Derivation protocol library.** Where a derivation protocol is reused across vessels, it MUST be registered with its provenance, its verification status and its known limitations.

### 18. Domain D-I — Version and drift

18.1 **Version lock.** Every claim MUST record instrument, case-law, class-notation and software versions. The approval basis MUST name the version of each instrument relied on.

18.2 **Change classification.** The approval basis MUST classify changes as: (1) requiring re-assessment; (2) pre-approved within declared bounds; (3) administrative. MUST state the bounds for pre-approved changes and the supporting evidence. MUST state that whether an Administration will accept bounded pre-approval is unknown and that no flag-State practice was found.

18.3 **Amendment horizon.** Register MUST record the amendment horizon for each instrument and the re-open trigger. MUST state an approval basis may be proved against a rule version that later changes.

18.4 **Case-law drift.** Register MUST record the case-law version and the re-open trigger if a higher or differently positioned court adopts a different interpretation.

18.5 **Class-notation drift.** Register MUST record the class-notation version and the re-open trigger on notation change.

18.6 **Software cadence.** A version-locked approval basis MUST declare how commercial-cadence software updates are handled within the change classification.

### 19. Domain D-J — Scope and application gate

19.1 The approval basis MUST record the application-gate decision (clause 10.2), the instruments found insufficient and the chapters invoked.

19.2 MUST record the scope decision (clause 10.3), the degrees of autonomy and transitions (clause 10.5), and national small-vessel measures (clause 10.7).

19.3 **Certificate and document register.** The approval basis MUST contain a register of statutory certificates, class certificates, ISM DOC/SMC, ISSC, and the Code's alternative document and certificate arrangements, as a view over the claim register.

19.4 **Port State control interface.** The approval basis MUST declare the approval passport: the summary the master or ROC produces to a PSC officer on request, the recognition route, and the contact route for the flag State or recognized organization. This is not a substitute for flag-State action.

19.5 **Approval withdrawal, suspension and condition change.** The approval basis MUST declare the procedure by which approval may be withdrawn, suspended or conditioned, and the operational consequence.

### 20. Domain D-K — Cyber, PNT and non-cooperative

20.1 **Cyber-induced degraded states.** Cyber risk assessment SHOULD be connected to COLREG-critical functions (downgraded from MUST; the Bridge calls the linkage an inference, not a statement in the instruments). Cyber-induced degraded states and their fallback and escalation routes MUST be declared where the submitter elects the linkage.

20.2 **PNT integrity (new, MUST).** MUST declare PNT integrity arrangements: GNSS integrity monitoring, spoofing and jamming detection, alternative PNT sources (for example radar, visual, inertial), holdover, degraded-state declaration and escalation. PNT denial MUST be treated as a sensor-sufficiency failure that triggers the Rule 5 fallback.

20.3 **AIS integrity.** MUST address AIS spoofing, latency and data quality, and the effect on the observables in D-C and D-D.

20.4 **Non-cooperative targets.** MUST address vessels that are non-compliant, deceptive or poorly detectable. MUST declare scenario-based V&V and escalation limits. MUST address the small, low-signature target case and MUST NOT assume camera or fused-sensor detection is sufficient without declared performance.

20.5 **Civil-military.** Warships and government ships are outside the MASS Code. This is recorded as an external watch item (Annex H) and as a scenario input to the harness, not as a claim.

### 21. Domain D-L — Liability and investigative evidence

21.1 **Pennsylvania.** Register MUST record the doctrine and later appellate formulations. MUST state application to autonomous look-out is for counsel.

21.2 **Causation.** MUST address causation questions raised by a defective navigation system, improper engagement or disengagement by an operator, or a system choosing between outcomes.

21.3 **Investigator usability.** The ledger MUST be investigator-usable. It MUST NOT claim court admissibility; it MUST claim integrity and usability and state its integrity method.

21.4 **Legal hold.** MUST declare the legal-hold procedure and post-casualty preservation.

### 22. Domain D-M — Communications (new)

22.1 **SOLAS IV and GMDSS.** MUST declare distress alerting, watchkeeping and shore maintenance arrangements in crewless and reduced-crew configurations.

22.2 **VHF watch and bridge-to-bridge.** MUST declare radiotelephony watch obligations, including the arrangement by which a crewless ship meets bridge-to-bridge communication expectations.

22.3 **Distress and SAR coordination.** MUST declare how the ship receives and responds to distress traffic, and the interface with SAR coordination.

22.4 **Communications failure.** MUST declare failure modes and fallback (including loss of control link) and the not-under-command signalling requirement noted in the Bridge (verification status recorded).

### 23. Domain D-N — Practical seamanship (new)

23.1 **Pilotage embarkation.** MUST declare the arrangement for compulsory pilotage, pilot embarkation and disembarkation, and the pilot's interface with the ANS and ROC. MUST address 46 U.S.C. § 8502 where US law applies.

23.2 **Anchoring and mooring.** MUST declare who anchors and moors, and the ANS support in those phases.

23.3 **SAR coordination.** MUST declare the ship's role as on-scene coordinator or assisting vessel where the duty to assist engages.

23.4 **Medical care for rescued persons.** MUST declare the accommodation, communication and medical support arrangements.

23.5 **Salvage and towage.** MUST declare the ship's obligations under salvage law and its ability to take or give a tow.

23.6 **Tug and escort operations.** MUST declare capability and limitations.

23.7 **Application.** Where a claim is not applicable (for example a fixed-route vessel never anchoring), it MUST be recorded as N/A with justification and owner.

#### v0.3 notes on sections 14–23 (as recorded in v0.3)

- **§15.2 (US work instruction).** Unchanged from v0.2: the 1 June 2026 work instruction is addressed as informative (SHOULD). The Red Team's H17 was addressed in v0.2.
- **§20.5 (civil-military).** Unchanged: civil-military is recorded as an external watch item (Annex H) and as a scenario input to the harness, not as a claim. Annex E no longer contains it (F18 fix).
- **§22.4 (communications failure).** Unchanged. (V&V results are required in the package at §5.2.5 and §27.9, not in §22.4.)
- **§23.7 (N/A).** Unchanged.

---

## 24. Runtime claim validity

24.1 Every closed or bounded claim MUST declare a runtime monitor.

24.2 A runtime monitor MUST be capable of detecting claim violation, threshold breach, confidence-band breach and fallback-state entry.

24.3 A claim violation MUST:

- raise an escalation event;
- record the event in the audit ledger with timestamp and time-architecture reference;
- re-open the claim;
- trigger the failure-mode response declared in the claim.

24.4 The runtime monitors are the operational bridge between UCFS and ARCVB.

24.4.1 The §24.4 bridge claim is a proposed claim, not an established one. Whether the ARCVB implementation actually performs the bridge is not verified in this framework. The claim is recorded as **[P] — proposed** and is an open item (Annex K2).

24.5 Runtime monitor evidence MUST be retained as an E4 stream.

24.6 **Runtime monitor gating.** The runtime monitors required by §24.1 are a gate requirement at G2 (§5.2.4). A claim without a specified, tested runtime monitor cannot close at G2.

---

## 25. Verification and validation harness

25.1 The harness MUST execute every closed and bounded claim.

25.2 **Scenario families (minimum):**

- crossing without intent to enter;
- shaping to enter on final approach (switch at the correct point);
- waiting for a pilot (crossing rules continue; no premature switch);
- give-way vessel on erratic course with steady bearing;
- already aligned and closing without detectable course adjustment;
- sensor degradation affecting bearing or closure rate;
- PNT denial or spoofing;
- AIS spoofing or latency;
- small, low-signature targets;
- non-cooperative, deceptive or poorly detectable targets;
- restricted visibility;
- cyber-induced degraded states;
- rule-set transition at a demarcation line;
- handover under maximum declared latency, including SA-rebuild segment;
- fleet-level multi-ship alarm load at the ROC;
- degraded-state reversion hysteresis;
- communications failure and distress response;
- anchoring, mooring, pilotage and tug scenarios where applicable.

25.3 The harness MUST record, per scenario: claim exercised, acceptance criterion, result, evidence artifact and evidence tier.

25.4 The harness MUST emit evidence in a form the ledger can retain.

25.5 The harness MUST NOT be presented as validated by any Administration or classification society unless it has been.

25.6 The harness MAY be shared with a conformance-mark policy (clause 28.6, Annex I) and a reference protocol library (clause 28.7).

25.7 The harness's V&V results are a package requirement at G6 (§5.2.5).

---

## 26. Audit ledger

26.1 The ledger MUST record every claim, its status, evidence, tier, owner, version lock, severity class and re-open trigger.

26.2 The ledger MUST record handover timestamps, authority transfer, SA-rebuild segments, escalation events, degraded-state transitions and PNT/time integrity events.

26.3 The ledger MUST record custody and access history of every evidence artifact.

26.4 The ledger MUST be tamper-evident. The integrity method MUST be declared: hash chain, signed append-only log, external timestamping, or a declared combination. "Tamper-evident" alone is not a method.

26.5 **Time architecture.** The ledger MUST declare:

- time source(s) and priority (GNSS, atomic, NTP, PTP, ship clock, ROC clock);
- synchronization method and frequency;
- drift bounds and holdover behaviour;
- integrity monitoring and detection of time-source denial or spoofing;
- fallback ordering.

26.5.1 Handover and latency claims MUST reference the time architecture.

26.6 **Tamper-evidence and integrity.** The ledger MUST record the hash algorithm, the signing keys and their custody, the timestamping method, and the audit trail of ledger administration.

26.7 **Availability.** The ledger MUST be available to the Administration and investigators on request, subject to the declared privilege posture in §26.8. Where a field is claimed privileged, the submitter MUST state the basis and the production route if the claim is challenged.

26.8 **Disclosure and privilege.** The submitter MUST declare, per jurisdiction:

- which ledger fields are produced to the Administration on request (regulatory evidence);
- which are safety-management records and their production basis;
- which are privileged risk assessments or legal interpretation memoranda;
- the legal-hold procedure;
- counsel sign-off.

26.8.1 UCFS MUST NOT assume the ledger is costless to create or uniformly producible. The disclosure posture is itself a claim (in D-H) with an owner, an acceptance criterion and a re-open trigger.

26.8.2 Where a jurisdiction's discovery rules would reach ledger fields the submitter claims privileged, the submitter MUST record that risk and the mitigation relied on.

26.8.3 **Acceptance criterion for counsel sign-off.** Counsel sign-off is satisfied only when a named counsel or legal office has reviewed the disclosure posture, recorded the date of review, and signed a statement that the declared privilege claims are supportable on the facts stated. The signature and the date are the criterion.

---

## 27. Approval Basis and ConOps package

27.1 The approval basis MUST be a view over the claim register, not a separate document with duplicated logic.

27.2 The ConOps MUST identify possible deviations from applicable rules and regulations and MUST justify alternative solutions on the basis of risk assessment.

27.3 The MASS Record MUST contain the regulatory gap analysis.

27.4 The package MUST contain, as views: the claim register, the responsibility matrix, the annexes (A–I), the certificate register, the PSC approval passport, the disclosure and privilege statement and the time architecture.

27.5 The package MUST distinguish interpretation from departure.

27.6 The package MUST state that its force comes from the Administration's approval and national implementation, not from the non-mandatory Code.

27.7 The package MUST be subject to re-assessment on change.

27.8 The package MUST declare its conformance vector, its conformance claim, and the version lock.

27.9 **V&V results.** The package MUST include V&V results for every closed and bounded claim, with evidence tier and artifact reference (§5.2.5).

---

## 28. Governance, re-assessment and openness

28.1 Open residues are reviewed at every gate. A closed or bounded claim MUST be re-opened on its trigger. Re-assessment MUST be recorded in the ledger.

28.2 Watch items are monitored by their monitoring owner. A watch item converts to a submitter-owned residue on its trigger.

28.3 **Experience-building.** A submitter SHOULD record and share anonymized reference test protocols for look-out equivalence, handover latency and rule-switching verification. Sharing MUST NOT be presented as creating a standard.

28.4 **Framework versioning.** UCFS clauses MUST be versioned. A clause change MUST identify the claims it affects and the re-assessment route.

28.5 **Stability commitment.** UCFS MUST NOT update faster than an annual cadence for substantive revisions. Defect corrections are recorded and dated, and are not subject to the annual cadence.

28.5.1 The annual cadence does not apply to defect corrections, which are recorded in the revision log with the defect identified and the correction made.

28.5.2 UCFS v0.1 → v0.2 → v0.3 are declared as a single development cycle. The v0.3 revision is a defect correction and a structural revision within that cycle. The annual cadence begins at v0.3.

28.6 **Conformance mark (suspended).**

28.6.1 The "UCFS-conformant" mark is suspended until Annex I is populated with a written policy. §28.6 of v0.2 is not operative.

28.6.2 A conformance claim under this framework MUST NOT use the phrase "UCFS-conformant" or any derivative until Annex I is populated.

28.7 **Reference protocol library.** A shared library of derivation protocols is planned. Its governance, provenance rules, verification status and confidentiality posture are open items (Annex K9, K10).

28.8 **Precedent sharing.** A shared precedent library raises antitrust and confidentiality issues. It is an open item (Annex K10).

28.9 UCFS MUST NOT be cited as an IMO instrument, a flag-State circular, a classification-society rule or a basis for certification.

---

## Annex A — Friction-to-domain conformance map

The Bridge's §3 frictions are listed with their UCFS domain, operators and a provisional flag where the source is unverified in the Bridge's §7.1 table. (v0.3 corrections to A1 and A7 are applied in the table and restated below it.)

| # | Bridge friction | Domain | Operators | Provisional |
|---|---|---|---|---|
| A1 | Rule 5 look-out: "sight and hearing" vs fused sensing; no machine benchmark | D-C.1 | APPLY, INTERPRET, ENCODE-OBSERVABLE, THRESHOLD, DERIVE, BOUND, RETAIN | — (Rule text verified; benchmark open) |
| A2 | Rule 2(a)/(b): immediate danger, remote judgment, no maximum latency; vessel limitations include sensors, ANS, link | D-A, D-E | INTERPRET, THRESHOLD, DERIVE, ESCALATE, OWN | — |
| A3 | Rule 6 safe speed: continuous judgment vs OE boundary | D-D | ENCODE-OBSERVABLE, THRESHOLD, DERIVE, BOUND | — |
| A4 | Rule 7(c) scanty information: no sensor-data threshold | D-C, D-D | THRESHOLD, DERIVE, DECLARE-OPEN | — |
| A5 | Rule 8: positive, ample time, readily apparent; succession of small alterations; *Ever Smart* timing | D-B, D-D | ENCODE-OBSERVABLE, THRESHOLD, DERIVE | [P] (*Ever Smart* not re-verified) |
| A6 | Rules 9/10: narrow channels, TSS, small MASS below 500 GT | D-A, D-J | ASSIGN-JURISDICTION, DECLARE-OPEN | — |
| A7 | Rule 17(a)(ii) observational vs 17(b) predictive | D-B, D-D.3 | ENCODE-OBSERVABLE, THRESHOLD, DERIVE, ESCALATE | [P] (*Ever Smart*) |
| A8 | Rule 19 restricted visibility: "detects by radar alone" vs fused sensing | D-C | ENCODE-OBSERVABLE, THRESHOLD, DERIVE | — |
| A9 | Parts C/D lights, shapes, sound signals; crewless activation; survey method | D-C | ENCODE-OBSERVABLE, OWN, RETAIN | [P] (Rules 32–37 text not read) |
| A10 | Part F verification at flag-State level vs vessel/ROC level | D-G | ASSIGN-JURISDICTION, VERSION-LOCK | [P] (heading-level only) |
| A11 | SOLAS V/19, V/20 electronic means; VDR; logged data | D-G | ENCODE-OBSERVABLE, VERSION-LOCK | [P] (not verified against consolidated text) |
| A12 | SOLAS II-1, II-2, III, V/33, XI-2/ISPS, IX/ISM | D-G | ENCODE-OBSERVABLE, OWN, VERSION-LOCK | [P] (not verified against consolidated text) |
| A13 | STCW: remote operators, ROC as bridge, remote experience, rest hours, seafarer question | D-E, D-G | THRESHOLD, DERIVE, DECLARE-OPEN | [P] (not verified against consolidated text) |
| A14 | MARPOL: no annex-by-annex mapping; Annex I/IV/V/VI; Protocol I duty | D-G | ENCODE-OBSERVABLE, OWN, RETAIN | [P]; IMO scoping output not found |
| A15 | Amendment drift 2023–2026 | D-I | VERSION-LOCK | [P] (not verified in this paper) |
| A16 | Application gate | D-J | ASSIGN-JURISDICTION, OWN | — |
| A17 | Layers of verification (III Code, Part F, XI-1/6, Code survey) | D-G | ASSIGN-JURISDICTION | [P] |
| A18 | Rule-set plurality | D-A, D-J | ASSIGN-JURISDICTION, ENCODE-OBSERVABLE | — |
| A19 | Cyber and non-cooperative targets | D-K | ENCODE-OBSERVABLE, BOUND, DECLARE-OPEN | Inference, not stated in instruments |
| A20 | Responsibility: flag State, Company, ROC, master, ANS; ISM quadrilateral; one ROC at a time; master for several ships | D-F | OWN, ESCALATE, THRESHOLD | [P] (IMO joint working group reported by GAO 2024) |
| A21 | US statutory complement | D-F | ASSIGN-JURISDICTION, OWN, VERSION-LOCK | — (verified against statutory text) |
| A22 | Canada, UK, Norway measures | D-F | ASSIGN-JURISDICTION | [P] (excerpts only) |
| A23 | *Pennsylvania* rule and causation | D-L | RETAIN, DECLARE-OPEN | — (doctrine verified) |
| A24 | GAO naval findings | D-H, D-I | THRESHOLD, OWN, VERSION-LOCK | Analogy only; [P] for testimony |
| A25 | Version-locked approval basis vs commercial software cadence | D-I | VERSION-LOCK | — |
| A26 | *Ever Smart* timing/legibility and steady bearing | D-B | ENCODE-OBSERVABLE | [P] |
| A27 | *Ever Smart* shaping-to-enter | D-B | ENCODE-OBSERVABLE, THRESHOLD, BOUND | [P] |
| A28 | *Ever Smart* two Rule 17 triggers | D-B | ENCODE-OBSERVABLE, THRESHOLD, ESCALATE | [P] |
| A29 | Appendix A placeholders | D-B | THRESHOLD, BOUND | Not validated |
| A30 | Bridge open substantive questions 1–10 | All | DECLARE-OPEN / DECLARE-WATCH (per Annex H) | — |
| A31 | SOLAS IV and GMDSS | D-G, D-M | ENCODE-OBSERVABLE, OWN | [P] (Bridge omits chapter IV) |
| A32 | VHF watch and bridge-to-bridge | D-M | ENCODE-OBSERVABLE | [P] |
| A33 | Pilotage embarkation | D-N | ENCODE-OBSERVABLE | — (§ 8502 verified) |
| A34 | Anchoring and mooring | D-N | ENCODE-OBSERVABLE, DECLARE-NA | — |
| A35 | SAR coordination and medical care | D-N | ENCODE-OBSERVABLE, OWN | — |
| A36 | Salvage and towage | D-N | ENCODE-OBSERVABLE, DECLARE-NA | — |
| A37 | Tug and escort | D-N | ENCODE-OBSERVABLE, DECLARE-NA | — |
| A38 | PNT integrity and GNSS denial | D-K | ENCODE-OBSERVABLE, BOUND | — |
| A39 | AIS spoofing and latency | D-K | ENCODE-OBSERVABLE, BOUND | — |

v0.3 corrections:

- **A1 (Rule 5):** Domain changed from D-C to D-C.1 (sub-item). Compression type field: application + interpretation.
- **A7 (Rule 17):** Domain changed from D-B, D-D to D-B, D-D.3.
- All [P] flags retained.

---

## Annex B — *Ever Smart* observable map

| Holding | Legal test | UCFS observable | Claim ref | Scope |
|---|---|---|---|---|
| Crossing vs narrow-channel (paras 134–145) | Displacement only when shaping to enter on final approach | Course adjustment to entrance; alignment on starboard side; closure | 11.3 | Governs in UK; elsewhere only if elected |
| Three situations | Crossing without intent; intending/preparing but not shaping; shaping | State machine: Crossing / Transition / Shaping | 11.3 | As above |
| Steady bearing (paras 111–112; 77–84, 108–112; conditions at 98(vi)–(vii)) | Crossing engages on steady bearing, not steady course; the vessel must be moving over the ground to some extent (98(vi)); where bearings cannot be taken over time the crossing rules may not be engaged (98(vii)) [P] | Bearing rate of change with declared accuracy; observability of bearings over time | 11.2 | As above |
| Rule 17(a)(ii) (para 61) | Permissive; the Bridge reads it as an observation problem [P] | Observation threshold; escalation | 11.5 | As above |
| Rule 17(b) (para 61) | Mandatory; the Bridge reads it as a prediction problem [P] | Prediction accuracy; tolerances; escalation | 11.5 | As above |
| Timing and legibility (para 40, *The Maloja II*) | No quick decision on inadequate information; readily apparent | Decision latency; range and timing | 11.6 | As above |

*Note (v0.2):* v0.1's universal formulation is withdrawn. The submitter MUST state the governing interpretation in the operating jurisdiction and MUST elect *Ever Smart* where it is not binding.

*Note (v0.3):* §11.1's "persuasive elsewhere" claim is now [P].

*Note (v0.3.1):* para 60 of the judgment concerns Rule 16, not Rule 17. The labels "observational" and "predictive" are the Bridge's engineering reading; the Court's wording is that the stand-on duty ends when it appears the give-way vessel is not complying, or when action by both vessels has become necessary. Paras 119 onward of the judgment have not been read (Bridge §7.1) [P].

---

## Annex C — MARPOL annex-by-annex register

| Annex | Obligation | Claim requirement | Status |
|---|---|---|---|
| I — oil | Discharge monitoring; IOPP | Automated monitoring and logging; IOPP survey treatment of unmanned spaces agreed with Administration | NW-4; survey treatment open |
| IV — sewage | Persons present | Zero-person periods; holding or reception; applies whenever persons present | Applies unchanged |
| V — garbage | Garbage management | Plan by voyage phase and person-presence mode | Applies unchanged |
| VI — air and efficiency | Emissions and efficiency | Propulsion type; compliance route; equivalence relied on | Applies unchanged |
| Protocol I | Immediate incident report | Reporting duty assigned; automated detection and logging | Data availability is not an immediate report; duty open |
| Annex-by-annex mapping | Code has none | Required in approval basis | IMO scoping output not found |

---

## Annex D — National-law and regulator-practice register

| Jurisdiction | Instrument | Claim requirement | Status |
|---|---|---|---|
| United States | 46 U.S.C. §§ 8101–8103, 8301, 8502, 4312; 2022 pilot; 46 C.F.R. §§ 15.715, 62.50; CG work instruction 1 June 2026; CG-ENG 01-23 | Statutory complement; legal route; ConOps and COLREGS statement; non-binding status of work instruction (SHOULD) | Verified; work instruction read in full |
| Canada | TP 13585 | Small autonomous surface ships; technical review board | Excerpts only |
| United Kingdom | SI 2023/1216 | Remotely operated unmanned vessels under 24 m; log book at ROC; exemptions and equivalences for larger ships | Excerpts only |
| Norway | RSV 12-2020 | Existing law by ship type; IMO equivalence process; reduced crew after tests | Excerpts only |
| Others | Not surveyed. Research priority order (non-binding, decision D2): Singapore, Japan, South Korea, China, Australia, then the large open registries [L, unverified], then Denmark and EU level | Declare whether surveyed | Open |

---

## Annex E — Submitter-owned open residues (revised)

| # | Residue | Domain | Severity | Owner expectation |
|---|---|---|---|---|
| E1 | Reference evidence for look-out equivalence | D-C.1 | S1 (NW-1) | Submitter + independent verifier |
| E2 | Handover latency threshold and SA-rebuild evidence | D-E | S2 | Submitter |
| E3 | Sensor-sufficiency threshold and uncertainty floor (vessel-specific) | D-C.2 | S1 (NW-1) | Submitter + independent verifier |
| E4 | Prediction-accuracy requirement for Rule 17(b) | D-D.3 | S1 (NW-2) | Submitter + independent verifier |
| E5 | MARPOL annex-by-annex mapping | D-G | S1 (NW-4) | Submitter |
| E6 | Small-MASS regime (beyond four surveyed jurisdictions) | D-J | S2 | Submitter |
| E7 | ROC workload and rest-hour quantification; multi-ship coverage; whether remote operators are seafarers under MLC 2006 is unexamined [P] | D-E | S2 | Submitter + ROC |
| E8 | Statutory flexibility for minimum-complement statutes | D-F | S1 (NW-3) | Submitter + flag State |
| E9 | *Pennsylvania* and causation application to MASS | D-L | S2 | Submitter + counsel |
| E10 | Bounded pre-approval of software changes | D-I | S1 (NW-8) | Submitter + Administration |
| E11 | Adoption of *Ever Smart* or a different observable trigger elsewhere | D-B | S2 | Submitter (jurisdiction-specific) |

**Removed from Annex E:** civil-military (E12 in v0.2). Per §20.5 and the UAIRF review F18, civil-military is a watch item (Annex H7), not a submitter-owned residue. The v0.2 Annex E E12 entry was a schema inconsistency.

---

## Annex F — Transition annex

**F1. Legal position.** Until a mandatory code is in force, the binding baseline is the existing conventions and national law. UCFS is a claim-and-evidence framework, not a compliance substitute.

**F2. COLREG stability.** COLREG was last amended in 2013. IMO's 2023 position, as reported in secondary summaries, was that COLREG requirements remain relevant and applicable regardless of how a ship is operated and that there was no need to amend COLREG to accommodate MASS at this stage [P] (v0.3 wording "no amendment is needed because COLREG can be applied in full" superseded; see §0.4.3). For planning purposes the Rules will not change before about 2032; this is a practical expectation, not a legal rule.

**F3. Harmonization by interpretation.** Harmonization will occur through interpretation in individual approvals, not amendment. The first Administrations to approve MASS with well-reasoned interpretations may set de facto practice. That is a prediction, not a finding.

**F4. National implementation.** Flag States may make the Code mandatory nationally, and contracts or class requirements may impose it earlier. Where they do not, the Code is applied unevenly while legacy duties remain binding. Certificates and approvals should say what was applied.

**F5. Statutes and pilots.** Where domestic statutes fix complement or credentials, relief currently comes from narrow pilot authorities (US 2022 at-sea recovery pilot) or statutory change.

**F6. Regulator practice.** Expect case-by-case review. The US Coast Guard's 2024 approach was to wait for the IMO framework and technology maturity; its 2026 work instruction reflects a more structured project-level process but is non-binding.

**F7.** MARPOL, small-MASS and ROC-workload items have no IMO-level resolution in this period; they will be handled by national practice and the approval basis.

**F8. Evidence accumulation.** The experience-building phase will be only as useful as the evidence it gathers. Submitters SHOULD record and share anonymized reference test protocols.

**F9. UCFS in transition.** UCFS v0.3 is written for the transition. When a mandatory code enters into force, UCFS MUST be revised to:

- reclassify application-gate claims that become mandatory;
- convert guidance-based claims to instrument-based claims;
- revise the non-waivable list to reflect the new instrument;
- revise Annex A's provisional flags.

**F10. Provisional conformance.** During the transition, a conformance claim MUST state that it is provisional and MUST identify the [P] clauses on which it relies.

---

## Annex G — Audience profiles

**G1. Administrations.** Focus on the claim register as the approval decision surface; use the non-waivable list to enforce minimums; use the conformance vector to calibrate review depth.

**G2. Recognized organizations and surveyors.** Focus on evidence tiers E2–E3, derivation protocols, and the runtime monitor evidence stream. Surveys verify declared thresholds are met and Parts C/D arrangements work as declared, including failure modes.

**G3. Operators and ROC providers.** Focus on runtime claim validity, handover latency and SA-rebuild evidence, ROC workload, and the disclosure posture.

**G4. Designers and autonomy developers.** Design for bearing-based engagement, separate Rule 17 logic, declared decision latency, explicit degraded states, PNT integrity and the evidence needed at the required tiers.

**G5. Insurers and underwriters.** Focus on bounded claims, severity classes, the non-waivable list and the runtime monitor stream. Engagement route is an open item (Annex K11).

**G6. Counsel.** Focus on compression types (application/interpretation/equivalence/departure), contestation and confidence, the *Ever Smart* scoping, the *Pennsylvania* clause and the disclosure and privilege statement.

---

## Annex H — External watch items

| # | Watch item | External actor(s) | Monitoring owner | Trigger to convert to residue |
|---|---|---|---|---|
| H1 | Whether IMO adopts a general sensor-sufficiency threshold | IMO | Submitter | MSC action |
| H2 | Whether the mandatory timeline (earliest 1 Jan 2032) holds | IMO | Submitter | MSC action |
| H3 | Whether other courts or Administrations adopt *Ever Smart* or a different observable trigger | Courts, Administrations | Submitter | Judgment or circular |
| H4 | MARPOL annex-by-annex mapping and IMO scoping output | IMO sub-committee | Submitter | Output published |
| H5 | Small-MASS regime development | IMO, national regulators | Submitter | Regime issued |
| H6 | Whether Administrations will accept bounded pre-approval | Administrations | Submitter | Policy or approval practice |
| H7 | Civil-military encounter conduct | States, IMO | Submitter | Guidance or incident |
| H8 | Statutory flexibility for minimum-complement statutes | Legislatures | Submitter | Amendment |
| H9 | IMO legal work on MASS liability | IMO | Submitter | Output |
| H10 | Class-notation convergence on autonomy | Class societies | Submitter | Notation publication |
| H11 | IMO LEG output on ROC jurisdiction and the flag-State / ROC-State relationship (CMI survey, April 2025, reports LEG 111/17 positions) [P] | IMO LEG; MSC | Submitter | Output or MSC action |
| H12 | EU AI Act, Cyber Resilience Act, NIS2 and Product Liability Directive timetable as applied to autonomy software [L, unverified] | EU institutions | Submitter | Official Journal text or application date (converts to K15) |
| H13 | Status of the IMO net-zero framework [L, unverified] | IMO MEPC | Submitter | MEPC action (converts to K17) |

---

## Annex I — Conformance-mark policy (outline)

**Suspended.** The mark is not available until this annex is populated with:

- the administering body;
- the required vector and evidence tiers;
- the audit or review required;
- the mark's trademark and licensing terms;
- the mark's withdrawal procedure;
- the mark's non-claim of legal compliance.

---

## Annex J — Resolution log (revised)

The v0.2 Annex J is retained as a historical record of the Red Team resolutions (see Annex M). The following table records the UAIRF v1.1 review findings and their v0.3 disposition. Each item is named individually; no item is claimed "addressed across clauses" without a specific reference.

| Finding | Disposition in v0.3 | Clause(s) |
|---|---|---|
| F1 (compression/status schema) | Fixed — separate attributes with mapping | §3.6–3.8, §8.2, §8.3.10 |
| F2 (application + interpretation) | Fixed — compression type set | §8.3.9, §12.1.1 |
| F3 (non-waivable severity conflict) | Fixed — residue S1, bounded claim S2 | §5.4.2, §8.8.3, §8.10.3 |
| F4 (E4 circularity) | Fixed — E4 obligation defined | §8.5.6 |
| F5 (off-list non-waivable) | Fixed — submitter obligation added | §5.4.3 |
| F6 (vector/gates circularity) | Fixed — vector is measurement; conformance is separate | §4.1.1–4.1.3, §4.2 |
| F7 (runtime not gated) | Fixed — G2 runtime monitor requirement | §5.2.4 |
| F8 (propagation method) | Fixed — derivation protocol required | §9.5.1, §13.6.1 |
| F9 (V&V not in package) | Fixed — V&V results required in package at G6 | §5.2.5, §25.7, §27.9 |
| F10 (conformance mark) | Fixed — suspended until Annex I populated | §28.6.1, §28.6.2 |
| F11 (failed→bounded conversion) | Fixed — conversion changes both attributes | §8.1.4 |
| F12 (N/A failure mode) | Fixed — exempt with reverse-evidence trigger | §8.4.3 |
| F13 (evidence sub-items) | Fixed — sub-items declared | §6.4, §8.5.5 |
| F14 (*Ever Smart* persuasive) | Fixed — claim narrowed and flagged [P] | §11.1.1 |
| F15 (Rule 19 fusion) | Fixed — derivation protocol required | §12.6.2 |
| F16 (two severity formulations) | Fixed — one rule | §8.8.3 |
| F17 (Annex E conditionals) | Fixed — S1 stated unconditionally | Annex E E8, E10 |
| F18 (civil-military in both annexes) | Fixed — removed from Annex E | Annex E |
| F19 (Annex J over-generalization) | Fixed — items named individually | This annex |
| F20 ([P] clearing) | Fixed — two routes declared | §2.2.2, §2.2.3 |
| F21 (confidence-band method) | Fixed — derivation protocol required | §8.11.5 |
| F22 (counsel sign-off) | Fixed — testable criterion added | §26.8.3 |
| F23 (bridge claim unverified) | Fixed — downgraded to [P] proposed | §24.4.1 |
| F24 (§26.7/§26.8 tension) | Fixed — §26.7 qualified | §26.7 |
| F25 (dimension independence) | Fixed — acknowledged | §4.2.4 |
| F26 (E4 obligation) | Fixed — defined | §8.5.6 |
| F27 (lineage method) | Fixed — declared | Annex L |
| F28 (internal authority field) | Open item — no clause written | Annex K12 |
| F29 (bounded fallback vs bounded) | Fixed — mapping declared | §8.3.10 |
| F30 (COLREG equivalence route) | Open item — not resolved by this framework | Annex K1 |
| U4 (annual-cadence self-violation) | Fixed — defect correction exception; single-cycle declaration | §28.5.1, §28.5.2 |
| GS2 (MSC.595(111) status conflict) | Fixed — reconciliation rule | §2.3 |
| SA1 (Red Team adoption claim) | Fixed — carve-outs unified | §0.1, this annex |
| SA2 (annual cadence) | Fixed | §28.5.2 |
| XR1 (class-society mapping) | Open item — no specific mapping in this framework | Annex K3 |
| TC1 (compression type vs status) | Fixed | §3.6–3.8 |
| TC2 (non-waivable formulation) | Fixed | §8.8.3 |

---

## Annex K — Open items (v0.3)

The following cannot be fixed within the framework without information or decisions not available to this draft. They are recorded here, not as operative clauses.

| # | Open item | Why it cannot be fixed here | Owner |
|---|---|---|---|
| K1 | Whether COLREG provides an equivalence route for Rule 5 | A legal question; the instruments do not state an equivalence route for COLREG, and UCFS cannot assert one | Submitter + counsel; flag State |
| K2 | Whether the ARCVB implementation performs the runtime bridge claimed in §24.4.1 | The ARCVB implementation is not examined in this framework | ARCVB implementer |
| K3 | The specific mapping between UCFS and class-society autonomy notations | No class-notation mapping is declared in the Bridge or in UCFS. v0.3.1 datapoint [P]: ClassNK's June 2026 explanatory decks on UR E26 describe a class documentation chain (asset inventory, zones and conduits, test procedure, programme approval). They cover cyber resilience only, not autonomy notations, and are secondary | Class societies; submitter |
| K4 | Whether an Administration will accept bounded pre-approval of software changes | No flag-State practice was identified in the Bridge | Administration |
| K5 | Whether the MASS Code's mandatory timeline (earliest 1 Jan 2032) holds | An IMO decision, not a framework decision | IMO |
| K6 | Whether IMO will adopt a general sensor-sufficiency threshold | An IMO decision | IMO |
| K7 | A full §24.6 self-application of UCFS to itself | Recommended by the UAIRF review; not performed in this revision | Author |
| K8 | Whether bounded claims in non-waivable domains should be permitted | v0.3 permits them as S2; the review flagged the underlying question as unresolved | Author + Administrations |
| K9 | Governance, provenance, verification status and confidentiality posture of a shared reference protocol library | Carried forward from v0.2; no governance decision has been made | Author |
| K10 | Antitrust and confidentiality posture for shared precedent | Carried forward from v0.2; no legal review has been made | Author + counsel |
| K11 | Insurer and underwriter engagement route | Carried forward from v0.2; no engagement has been made | Author |
| K12 | Internal-authority field for non-hierarchical documents (F28) and for UCFS itself | No clause was written in v0.3; §7.11.5 and §12.20 as cited in the v0.3 draft do not exist in UCFS. UAIRF v1.1 §7.11 (internal authority hierarchy field) and §12.20 (register) now exist and are a candidate model [P]; no clause written | Author |
| K13 | Commercial and civil-law regimes are unmapped: carriage of goods (Hague-Visby, US COGSA, Rotterdam), bills of lading, electronic transferable records, charterparties, ship-management contracts, marine insurance, general average, salvage, liens (gap map W1-01 to 10, 12, 14). Decision D5: if mapped, they go in a companion document, not UCFS | UCFS D-A to D-N cover safety and statutory approval only | Author; counsel |
| K14 | Registry, cabotage, SAR and security-law regimes unmapped (gap map W2-02 to 05) | No UCFS domain | Author; flag States; counsel |
| K15 | Non-IMO standards and digital regulation unmapped: IMO cyber instruments, IEC/ISO, e-navigation data, radio and control-link regulation, GNSS/PNT standards, type approval, EU AI Act / CRA / NIS2 / product liability, remote inspection and e-certificates (gap map W3-02, 03, 05 to 10). H12 converts to K15 on its trigger | Only IACS UR E26/E27 has been touched (see K22) | Author |
| K16 | Cargo and vessel-type regimes, and a scope matrix of ship type × trade × degree × jurisdiction (gap map W4-01 to 06) | Not mapped | Author |
| K17 | Environmental and carbon regulation beyond MARPOL: ballast water, anti-fouling, recycling, CII/EEXI/ETS/FuelEU, underwater noise (gap map W5-02 to 04). H13 converts to K17 on its trigger | Not mapped | Author |
| K18 | Port and facilitation regimes: FAL, customs and border filings, health and quarantine, pilotage and VTS bylaws, towage and terminal acceptance (gap map W6-01, 02, 03, 05, 06) | Not mapped | Author |
| K19 | Industry vetting, war-risk and sanctions practice (gap map W7-01 to 03) | Not mapped; could bar a MASS regardless of Administration approval | Author |
| K20 | Depth imbalance: UCFS is deep on COLREG and shallow elsewhere (gap map §5 item 6) | Either deepen other domains or label them lower-resolution | Author |
| K21 | Export controls on autonomy software and sensors (gap map W9-03) | Not mapped | Author |
| K22 | Whether UR E26/E27 cyber scope over navigation systems changes the status of the §20.1 "inference" wording | ClassNK explanatory decks say navigation systems are in E26 scope (a class requirement, secondary source); they do not mention COLREG. UR E26/E27 text unread. §20.1 not changed | Author; class societies |
| K23 | Scope boundary: subsea ROV, AUV and uncrewed submersibles (gap map W9-01) are outside this stack (decision D3, 15 Nov 2026) | Re-open if deep-vehicle regulatory mapping is needed; a companion document would then be opened | Author |

---

## Annex L — Lineage declaration (F27)

**L1. Version comparison method.** v0.1 → v0.2 → v0.3 comparisons were performed by itemised carry-forward list for the Red Team findings and the UAIRF findings, with clause-level cross-reference.

**L2. v0.1 → v0.2.** v0.2 adopted the Red Team Report "in full except where noted in clause 0.4." As the UAIRF review found (SA1), the carve-out also excluded clause 0.3's non-adoptions; the "in full" claim was therefore narrower than stated. v0.3 corrects the record (see Annex J).

**L3. v0.2 → v0.3.** v0.3 applies the UAIRF review findings F1–F30. Each finding is named individually in Annex J with its disposition and clause reference. Findings that could not be fixed are recorded in Annex K.

**L4. No silent drops.** The v0.3 revision claims no silent drops of v0.2 clauses. The specific changes are: the schema reconciliation (§3, §8.2, §8.3), the severity rule (§5.4.2, §8.8.3, §8.10.3), the E4 obligation (§8.5.6), the sub-items (§6.4), the narrowed *Ever Smart* claim (§11.1.1), the Rule 19 fusion derivation (§12.6.2), the confidence-band derivation (§8.11.5), the §26.7 qualification, the §28.6 suspension, the Annex E removal of civil-military, and the addition of Annexes K and L.

**L5. Limits.** This lineage declaration is not independent verification. It is the author's own comparison. Under UAIRF §26.6, a completeness claim requires a stated method; the method is declared in L1, and the limits are declared here.

**L6. Merge revision.** The v0.2 text for every section marked "unchanged from v0.2" was merged into this file, and the differences between v0.2 and v0.3 were reviewed. The corrections made are listed in §0.1.27 and Annex Z. This comparison is the author's own, not independent verification.

**L7. v0.3 → v0.3.1.** Method: SHA-256 of the prior file (`69fb4485d943ed9467a78ad04c579bdf311866b3fceb375723b8032048487ccd`), a line diff, and the itemised list in §0.4. The hash of this file is recorded outside it, so the chain is one-directional (UAIRF v1.1 §26.6): a reader can verify the prior version but must take the new file's hash from the update report. Limits: same-collaborator production; Annex P is not independently reviewed; "no silent drops" is supported only by the diff and §0.4 and is not independently verified.

---

## Annex M — Red Team resolution log (carried forward)

The v0.2 Annex J (Red Team resolution log) is carried forward unchanged, with the following note: the UAIRF review F19 found that the v0.2 Annex J's M1–M22 claim was over-general. The v0.3 Annex J (the UAIRF resolution log) names each finding individually. The Red Team resolution log is retained here as a historical record and is not re-asserted as a completeness claim.

| Red Team item | Resolution in v0.2 |
|---|---|
| C1 (negative outcome) | Fourth status "failed"; non-waivable list (clause 5.4); severity classes (clause 8.8) |
| C2 (declaration theater) | Derivation protocol (clause 8.6); evidence tiers (clause 8.5); reference protocol library expectation |
| C3 (equivalence confusion) | Rule 5 defaulted to application + interpretation; equivalence reserved for formal SOLAS-style routes (clause 12.1) |
| C4 (evidence hierarchy) | E1–E4 tiers with minimums by domain (clause 8.5) |
| C5 (unverified premises) | [P] provisional flag (clause 2.2) applied throughout |
| C6 (gate waiver) | Gate integrity rule (clause 5.5) |
| C7 (discoverability and privilege) | Disclosure and privilege clause (clause 26.8) |
| C8 (time and integrity) | Time architecture (clause 26.5) and tamper-evidence method (clause 26.6) |
| H1 (ladder) | Five-dimension vector (clause 4.2) |
| H2 (consistency) | Consistency rule (clause 9.6) |
| H3 (runtime validity) | Clause 24 |
| H4 (failure modes) | Clause 8.4 |
| H5 (uncertainty propagation) | Clause 9.5 and 13.6 |
| H6 (sensor-sufficiency derivation) | Clause 12.3 and clause 8.6 |
| H7 (handover event chain) | Clause 14.1, 14.2 |
| H8 (PNT and AIS) | Clause 20.2, 20.3 |
| H9 (SOLAS IV and GMDSS) | Clause 16.5 and D-M (clause 22) |
| H10 (seamanship) | D-N (clause 23) |
| H11 (PSC) | Clause 19.4 |
| H12 (certificate register) | Clause 19.3 |
| H13 (residue vs watch item) | Clauses 8.8, 8.9; Annex E and Annex H |
| H14 (N/A) | Clause 8.1.1 and clause 23.7 |
| H15 (contestation and confidence) | Clause 8.11 |
| H16 (*Ever Smart* overreach) | Clause 11.1; Annex B scoped |
| H17 (work instruction overreach) | Clause 15.2 (SHOULD, informative) |
| H18 (cyber overreach) | Clause 20.1 (SHOULD) |
| H19 (civil-military) | Clause 20.5 (watch item, not claim) |
| H20 (transition) | Annex F |
| H21 (audience profiles) | Annex G |
| H22 (class-society positioning) | Clause 1.8 |
| M1–M22 | Addressed across clauses 8.6, 8.11, 12.7, 13.3, 12.6, 22, 24, 26, 28; class-notation drift added at 18.5 |
| L1–L7 | Glossary expanded; date header added; Annex H removes predictions from residues; notes separated from claims; status carried forward per row; blueprint language corrected in clause 1.4.4 and clause 21.3; "viral" framing not adopted |

*(Clause numbers in this table are v0.2 numbers.)*

---

## Annex P — Proposed clauses (v0.3.1; non-operative)

**Status.** Nothing in this annex binds a conformance claim. Each proposal is a candidate for the next substantive revision under §28.5 and is [P] until its sources are verified (§2.2). Domain, evidence tier and derivation-protocol requirement are stated for each, as the intake process required. No proposal has been reviewed independently.

| ID | Proposed clause | Domain | Evidence tier | Derivation protocol | Basis and limits [P] |
|---|---|---|---|---|---|
| P-1 | **Proposed §15.6, ROC location and jurisdiction.** The register MUST declare the State in which each ROC is located, its relation to the flag State, the route by which the flag State exercises certification, survey and audit over the ROC, and any flag-State / ROC-State arrangement relied on | D-F | E1 (declaration); a route found workable by the Administration needs E2 | None; no threshold is involved | CMI survey of 12 States to MSC 110 (7 April 2025): anonymised, predates the Code, and its UNCLOS article numbers are inconsistent (Arts 92/94 in Q1, 91/94 in the overview). UNCLOS text unread |
| P-2 | **Proposed §20.6, class cyber-resilience applicability.** Where a ship is contracted on or after 1 July 2024 and within IACS UR E26 scope, the register MUST record which computer-based systems are in scope, the class approval status of the ship's cyber security and resilience programme, and the UR E27 approval status of in-scope equipment | D-K | E2; E3 where class-witnessed | None | ClassNK explanatory decks (June 2026), secondary. UR E26/E27 text unread (see K22) |
| P-3 | **Proposed addition to §19.3.** The certificate register MUST include civil-liability certificates (for example CLC, Bunkers, Nairobi WRC) and the State that issued each | D-J | E1 | None | MLETR Explanatory Note fn. 32 describes such certificates as administrative documents, not transferable instruments. Convention texts unread |
| P-4 | **Proposed Annex N, standards register.** A register of non-IMO standards and forms a claim relies on (IACS URs, IEC/ISO, class notations, BIMCO forms, e-document statutes), with version and verification status | D-H | E1 | Registration with provenance, as §17.7 | Gap map §6 item 3. Content of the register not yet researched (K15) |
| P-5 | **Proposed addition to §11, "in sight" and fusion.** A claim relying on the crossing rules MUST declare which fusion states count as "in sight" for Section II, the rule set applied when a target is detected only by sensors, and how bearing steadiness is measured. Split by §6.1 into one claim per domain (D-B and D-C) | D-B; D-C | E2 | REQUIRED for the fusion-state definition (as §12.6.2) | Bridge §4.1, citing Rule 3(k) and judgment paras 46 and 72–73. Judgment paras read by the Bridge author only [P] |
| P-6 | **Proposed extension of §11.2, observability.** A crossing-engagement claim MUST state the conditions under which bearings are observable over time and whether the vessel is moving over the ground (judgment paras 98(vi)–(vii)) | D-B | E2 | Bearing-rate accuracy under §8.6 (already required by §11.2) | Bridge corrections A2; paras 98(vi)–(vii) read by the Bridge author only [P] |

---

*End of UCFS v0.3.1.*

---

## Summary of what changed and what remains open

**Fixed in v0.3:**

- Schema reconciliation: compression type set vs status, with a normative mapping table (§8.3.10).
- Non-waivable severity: residues S1, bounded claims S2, with one formulation (§8.8.3).
- E4 obligation: fully defined (§8.5.6).
- Conformance vector: measurement, not conformance claim (§4.1–4.3).
- Runtime monitors: gated at G2 (§5.2.4).
- V&V results: in the package (§27.9).
- Derivation protocols: required for propagation, confidence bands, Rule 19 fusion (§9.5.1, §8.11.5, §12.6.2).
- [P] clearing: two routes (§2.2.2).
- *Ever Smart* persuasive claim: narrowed and flagged [P] (§11.1.1).
- Conformance mark: suspended (§28.6.1).
- Civil-military: removed from Annex E (§20.5, Annex H).
- Annex J: findings named individually, not "addressed across clauses."
- Annual cadence: defect-correction exception and single-cycle declaration (§28.5).
- Annexes K (open items) and L (lineage) added.

**Remains open (Annex K):**

- K1: COLREG equivalence route — legal question.
- K2: ARCVB runtime bridge — implementation not examined.
- K3: Class-notation mapping — not declared.
- K4: Bounded software pre-approval — Administration decision.
- K5: MASS Code timeline — IMO decision.
- K6: General sensor-sufficiency threshold — IMO decision.
- K7: UCFS self-application — recommended, not performed.
- K8: Bounded claims in non-waivable domains — design choice, not legal resolution.
- K9: Reference protocol library governance — carried forward from v0.2.
- K10: Antitrust and confidentiality posture for shared precedent — carried forward from v0.2.
- K11: Insurer and underwriter engagement route — carried forward from v0.2.
- K12: Internal-authority field (F28) — no clause written.

**One further honest note.** This v0.3 is produced by the same collaborator that produced v0.1 and v0.2 and the UAIRF review. Under UAIRF §25.3, it is development evidence, not independent corroboration. The framework's own §28.5.2 now allows the annual cadence to begin at v0.3; a future independent review is the next step that would strengthen the framework's claims.


---

## Annex Z — Merge change record (non-normative)

*This annex is not part of UCFS v0.3. It records what the merge of v0.2 into v0.3 found and what was done about it.*

### Z1. Restored from v0.2

| # | Restored text | Now at |
|---|---|---|
| Z1.1 | Definitions of Closed, Bounded, Failed / operation not permitted | §3.35, §3.36, §3.37 |
| Z1.2 | "MUST NOT be read as permission to suppress or average away uncertainty" | §3.4.1 |
| Z1.3 | Red Team non-adoptions (rename of "Compression"; opening the harness early) | §0.2.3, §0.2.4 |
| Z1.4 | Open items: protocol-library governance; antitrust and confidentiality; insurer engagement | Annex K9, K10, K11 (and §0.3) |

### Z2. Corrected in the text

| # | Correction |
|---|---|
| Z2.1 | F28 / §7.11.5: no such clause exists. The "Fixed" disposition was replaced with "Open item" (Annex K12); §0.1.23, §0.2.1 and Annex J updated; the §12.20 reference removed. |
| Z2.2 | §12.3.4 reference in K6 changed to §13.2. |
| Z2.3 | F9: V&V results are cited at §5.2.5, §25.7 and §27.9, not §22.4 (§0.1.8, Annex J, note on §22.4). |
| Z2.4 | §2.2.2(a): the "(§9.6)" cross-reference removed; the verification record is now described inline (source, primary or official text consulted, date, result). |
| Z2.5 | §0.1.1: mapping now cites §8.3.10. |
| Z2.6 | K4: §18.2.2 changed to §18.2. |
| Z2.7 | The "7.1–7.3" source notes removed; §7 has 7.1, 7.2 and 7.4 only. |
| Z3.1 | §9.6: a consistency conflict is an open residue whose severity class is assigned under §8.8.3 (previously "an S1 residue"). §9.16 is unchanged. |
| Z3.2 | Annex E: conditional wording removed from E1, E3, E4 and E5; all four are stated as S1 (as E8 and E10 already were). |
| Z3.3 | "Class C+" retired in the header, §2.2.2, §11.1.1 and Annex F F10. A [P] clause now cannot support any conformance claim until cleared under §2.2.2. |
| Z3.4 | Cross-references corrected: §11.3 (→ §25), §14.4 and §17.6 (→ §26.5), §25.6 (→ §28.6, §28.7). |
| Z3.5 | Stale version language updated: Annex F F9 ("v0.3"), Annex G5, §28.7 and §28.8 (now point to Annex K). |

### Z3. Decisions to confirm

- **§9.6 (Z3.1).** The change above follows §8.8.3 as written in v0.3. If you intended a consistency conflict to always block the gate, restore the v0.2 S1 wording and reconcile §8.8.3 instead.
- **§2.2.2(a) (Z2.4).** The inline description of a verification record is a minimal definition added in this pass, not v0.2 or v0.3 text.
- **Z3.3.** Retiring "Class C+" makes the [P] rule stricter (it now applies to every conformance claim). If a minimum level was intended, define the level in §4 instead.
- **K12.** F28 was moved to an open item rather than writing a new §7.11.5.

### Z4. Left as received

- v0.2 §8.8.2–8.8.3 (S1 as a residue that "otherwise prevents safe operation"; the severity-floor rule) is not restored; v0.3's narrowing under F3 stands.
- Minor v0.2 drops not restored: the §1.4.4 sentences "Compliance is established by the instrument and the approving Administration. UCFS structures the claim and its evidence."; §4.2.4–4.2.5; §1.8.3 mapping phrase; the §28.5 last sentence; Annex I I1 and I3; the Annex E footer; the v0.2 §8.3.8 required content for failed claims.
- Annex M keeps M1–M22 and L1–L7 as the grouped rows in the v0.2 source.
- The closing remark in the v0.2 source (an offer to produce clause-level test assertions) is a chat remark and is not included.

### Z5. Decisions on the Z3 items (added v0.3.1)

These were delegated by the author on 15 November 2026 and approved with the v0.3.1 update plan. They are the author's decisions as executed by the collaborator, not independent review.

| # | Item | Decision | Effect |
|---|---|---|---|
| Z5.1 | §9.6 consistency conflict severity (Z3.1) | Keep the §8.8.3 rule: S1 in a non-waivable domain, otherwise S2 or S3 by justification. Always-S1 would reopen F3 and F16 | No change |
| Z5.2 | §2.2.2(a) inline verification-record definition (Z2.4) | Keep. A record MAY follow the UAIRF v1.1 §9.6 format; this is not a requirement | No change |
| Z5.3 | "Class C+" (Z3.3) | Accept the stricter rule: a [P] clause cannot support any conformance claim until cleared under §2.2.2. IAAP v0.2.1 A-12 still said "Class C+" and is corrected in IAAP v0.2.2 | No change to UCFS |
| Z5.4 | K12 (F28) | Remains an open item. UAIRF v1.1 §7.11 and §12.20 are recorded as a candidate model; no clause written | K12 text updated |
