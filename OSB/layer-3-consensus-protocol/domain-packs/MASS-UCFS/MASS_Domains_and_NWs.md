# MASS-UCFS Domain Pack — extracted from UCFS v0.3.1

| Field | Value |
|---|---|
| Document | MASS domain pack for the UCFS v0.3.1 modular layout |
| Status | Editorial extraction; not a new UCFS revision, independent review, or verification upgrade |
| Source | The unchanged full source is [archived here](../../source/UCFS_v0.3.1_Full_Source.md) |
| Purpose | Preserve MASS domain definitions, non-waivable list, domain evidence minima, domain clauses, and supporting annexes outside the shared core |
| Numbering | Original section and annex numbers are retained so existing references can be traced |

> **Use with the core.** Shared claim, gate, evidence, provisional-status, ledger, and governance rules remain in [UCFS_Core_v0.3.1.md](../../UCFS_Core_v0.3.1.md). The passages below are copied from the full source; the core contains routing notes where these passages were extracted. Check the archived full source when comparing wording or resolving references.

## Extracted provisions
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

### 8.5 Evidence tiers

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

8.5.7 An Administration MAY raise a minimum tier. It MUST NOT lower the tiers for NW-1, NW-2, NW-3, NW-4 or NW-5.

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
