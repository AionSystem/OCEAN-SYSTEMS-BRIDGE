# ARCVB v0.1 — Automated Regulatory Compliance & Verification Bridge

**Implementation architecture specification. Child of UCFS v0.3.**

| Field | Value |
|---|---|
| Document | ARCVB v0.1 — implementation architecture specification (full, non-compressed) |
| Supersedes | "Project Blueprint: The Automated Regulatory Compliance & Verification Bridge (ARCVB)" (informal blueprint) |
| Parent | UCFS v0.3 — Uncertainty Compression Framework/Spec. UCFS defines what a claim, its evidence and its runtime monitoring MUST contain. ARCVB specifies how a system can produce, test, monitor and record them. |
| Source map | The MASS Regulatory Bridge (13 Nov 2026) is the friction and evidence source map for UCFS and, through it, for ARCVB. |
| Status | Draft for technical review. Not a standard. Not legal advice. Not endorsed by any Administration, recognized organization or classification society. Not a basis for certification. Does not establish that any ship complies with any instrument. |
| Conventions | MUST, MUST NOT, SHOULD, SHOULD NOT, MAY in the RFC 2119 sense. |
| Provisional flag | **[P]** is inherited from UCFS §2.2. An ARCVB clause that rests on a [P] source or on a [P] UCFS clause is itself [P] and cannot support a conformance claim until cleared under UCFS §2.2.2. |
| Requirement IDs | Each normative requirement carries an ID of the form `ARCVB-<area>-<nn>` and a trace to the UCFS clause it implements, so that a test assertion can be written against it one-to-one. |
| Date | 14 November 2026 |

---

## 0. Changes from the blueprint

The blueprint is the informal source of this specification. Where a blueprint statement conflicts with UCFS v0.3, UCFS governs and the statement is changed here. The changes are recorded, not silently made.

### 0.1 Disposition of blueprint statements

| # | Blueprint statement | Disposition in ARCVB v0.1 | Basis |
|---|---|---|---|
| 0.1.1 | "Continuously prove legal compliance" | Changed. ARCVB produces and maintains declared claims, evidence and runtime monitoring. Compliance is established by the instrument and the approving Administration, not by ARCVB. | UCFS §1.4.4, §4.2 |
| 0.1.2 | "Court-admissible audit trails" | Changed to **tamper-evident, investigator-usable** records. ARCVB MUST NOT claim court admissibility. | UCFS §21.3 |
| 0.1.3 | "Mathematically verifiable regulatory approvals" | Changed. ARCVB produces claims with declared evidence tiers (E1–E4) that a reviewer can re-execute. Approval remains the Administration's decision. | UCFS §8.5, §27.6 |
| 0.1.4 | "Unified, deterministic middleware" | Narrowed. Determinism is claimed only for the rule-state and monitor logic, given identical inputs and an identical version lock (§3.4). Perception inputs are not deterministic and are not claimed to be. | Design choice (§3.4) |
| 0.1.5 | Layer 1 includes "Ever Smart Case Law" and "IMO MASS Code" | Scoped. *Ever Smart* holdings are UK law and are used only where the submitter states the governing interpretation or elects it (UCFS §11.1). The MASS Code is guidance **[P]**. | UCFS §1.5, §11.1 |
| 0.1.6 | Subsystem A: "sustained course changes (≥ 5° over 60 seconds)" as the transition rule | Changed. The figure is retained only as an **illustrative placeholder** and is not a threshold. *Ever Smart*'s test is shaping to enter on final approach and steady *bearing*, not a course-change figure. Every threshold needs a derivation protocol. | UCFS §8.6, §11.2, §11.3, Annex A (A29) |
| 0.1.7 | Subsystem A: "prevents the ANS from applying illegal assumptions" | Changed to: makes assumptions declared, observable and testable. ARCVB does not guarantee legality of any manoeuvre. | UCFS §1.4.4 |
| 0.1.8 | Subsystem B named "Look-Out **Equivalence** & Sensor Sufficiency Engine" | Renamed **Look-Out & Sensor-Sufficiency Engine**. The default compression type for Rule 5 is application + interpretation, not equivalence. Equivalence is available only if a formal COLREG equivalence route is identified, which UCFS does not assume exists. | UCFS §8.3.3, §12.1, Annex K1 |
| 0.1.9 | Subsystem B: engine "shifts the ship into a pre-declared degraded/fallback state" | Clarified. The engine declares the sufficiency state and raises the escalation event. Who executes the fallback (the ANS or ARCVB) depends on the integration mode (§4.3). | UCFS §8.10, §24 |
| 0.1.10 | Subsystem C: ledger "proves due diligence" and "mitigates" *The Pennsylvania* | Changed. The ledger preserves evidence. Its effect on liability is a question for counsel. | UCFS §21.1, §21.2 |
| 0.1.11 | Subsystem D: three change classes | Retained and mapped to UCFS §18.2. Whether an Administration will accept bounded pre-approval is unknown. | UCFS §18.2, Annex K4 |
| 0.1.12 | "Generate an IMO-compliant approval package in hours instead of months" | Removed. No such time claim is supported, and an approval package is not "IMO-compliant" by being generated. ARCVB generates the approval basis as a **view over the claim register**. | UCFS §1.4.4, §27.1 |
| 0.1.13 | §4 "How to make it viral" (open-source harness first; standard schema; dual-use targeting) | Replaced by §10 (openness and adoption). Opening the harness before the claim model is stable, and before a conformance-mark policy exists, was not adopted at UCFS v0.2/v0.3. | UCFS §0.2.4, §28.6, Annex I |
| 0.1.14 | "Defense contractors" and "uncrewed vessel program offices" as an audience | Retained only as a dual-use note (§10.4). Warships and government ships are outside the MASS Code; civil-military conduct is an external watch item. | UCFS §20.5, Annex H7 |

### 0.2 Added to the blueprint

The blueprint's four layers and four subsystems are kept. v0.1 adds:

- a claim register service and a consistency checker (§6.1);
- a runtime monitor service (§6.2), because UCFS §24 makes runtime monitors a gate requirement at G2;
- a time service (§6.3), because UCFS §26.5 and NW-7 require a declared time architecture;
- a package generator (§6.9), because UCFS §27.1 requires the approval basis to be a view;
- integration modes (§4.3), because the blueprint does not say whether ARCVB sits inside or beside the safety chain;
- ARCVB's own failure behaviour (§8);
- a requirement ID scheme and a traceability matrix (Annex B).

---

## 1. Scope, purpose and positioning

### 1.1 Purpose

1.1.1 ARCVB is a software and process architecture that sits between an autonomous navigation system (ANS) and the regulatory framework that governs the ship (COLREG, SOLAS, MARPOL, the ISM and ISPS Codes, STCW, load-line and statutory manning law, as listed in UCFS §1.3).

1.1.2 ARCVB's purpose is to produce, test, monitor and record the claims that UCFS requires, and to keep them true during operation (UCFS §24).

1.1.3 ARCVB is the implementation pipeline of UCFS. UCFS is the parent specification.

### 1.2 What ARCVB is not

1.2.1 ARCVB is not an ANS. It does not plan or execute navigation (except in integration mode M3, which this version does not specify; §4.3.5).

1.2.2 ARCVB does not replace Administration approval, class approval or survey (UCFS §1.4.2, §1.8.2).

1.2.3 ARCVB does not determine legal liability (UCFS §1.4.1).

1.2.4 ARCVB MUST NOT be presented as evidence that a ship complies with any instrument (UCFS §1.4.4).

### 1.3 Application

1.3.1 This specification applies to an ARCVB implementation deployed for a MASS, for a remote operations centre (ROC), or for an approval or audit activity on either.

1.3.2 Application is limited to the scope in UCFS §1.2: MASS within the Code's scope, and small MASS only where national small-vessel measures are declared (UCFS §10.3, §10.7).

---

## 2. Normative references

2.1 UCFS v0.3 and every instrument it lists in its §2.1, with the verification status UCFS records. ARCVB does not upgrade any source's status (UCFS §1.7.3, §9.13).

2.2 The informal blueprint named on the title page, as the source of §0.

2.3 Where this specification and UCFS disagree, UCFS governs.

---

## 3. Terms and definitions

UCFS definitions (UCFS §3) apply. The following are specific to ARCVB.

3.1 **ARCVB core** — the software services that perform the functions in §5 and §6.

3.2 **Rule state** — the declared set of rules the ARCVB core treats as governing the ship's relationship to a given target or area at a given time (for example *Crossing*, *Transition*, *Shaping to enter*), with its confidence band (UCFS Annex B).

3.3 **Sufficiency state** — the declared state of the sensor suite relative to the sensor-sufficiency threshold and uncertainty floor: *sufficient*, *degraded* (with level) or *insufficient* (UCFS §3.28, §3.32).

3.4 **Determinism scope** — the part of the ARCVB core for which an identical input stream, identical configuration and identical version lock MUST produce an identical output stream. The determinism scope is the rule-state machine, the sufficiency evaluation, the runtime monitors and the ledger writer. It excludes sensor hardware, perception models and any component using a stochastic method that does not declare a seed.

3.5 **Integration mode** — M0, M1, M2 or M3 as defined in §4.3.

3.6 **Authority state** — which actor holds navigational authority at a time: ANS, ROC operator, master on board, or a declared intermediate state.

3.7 **Escalation event** — an event raised under UCFS §24.3: a claim violation, threshold breach, confidence-band breach or fallback-state entry.

3.8 **Version manifest** — the machine-readable list of instrument versions, case-law versions, class-notation versions and software versions that make up a vessel's version lock (UCFS §3.33).

3.9 **Reference vessel register** — a claim register for a named vessel or for a declared test vessel, used to exercise the ARCVB core without an operational claim.

---

## 4. Architecture

### 4.1 Layers

The blueprint's four layers are retained.

```
+-----------------------------------------------------------------+
| LAYER 1 — REGULATORY LAYER                                      |
| Source registry, claim register, jurisdiction and version lock  |
| (instruments, MASS Code [P], case law scoped by jurisdiction,   |
|  flag State, class notations)                                   |
+-----------------------------------------------------------------+
                               |
                               v
+-----------------------------------------------------------------+
| LAYER 2 — TRANSLATION ENGINE                                    |
| Rule-state machine; look-out and sensor-sufficiency engine;     |
| handover/authority tracker                                      |
+-----------------------------------------------------------------+
                               |
                               v
+-----------------------------------------------------------------+
| LAYER 3 — VERIFICATION AND V&V HARNESS                          |
| Scenario execution; evidence artifact generation; evidence tiers|
+-----------------------------------------------------------------+
                               |
                               v
+-----------------------------------------------------------------+
| LAYER 4 — UNIFIED AUDIT LEDGER                                  |
| Tamper-evident records; responsibility matrix; investigator view|
+-----------------------------------------------------------------+

 Cross-cutting services: claim register service and consistency
 checker · runtime monitor service · time service · version-lock
 and drift mapper · package generator
```

### 4.2 Layer rules

| ID | Requirement | UCFS trace |
|---|---|---|
| ARCVB-ARCH-01 | Layer 1 MUST be the only source of claim definitions. Layers 2–4 MUST reference claims by claim identifier and MUST NOT duplicate claim logic. | §27.1 |
| ARCVB-ARCH-02 | Layer 2 outputs MUST carry the claim identifier of the claim they evidence or monitor, the version lock in force, and a time-service reference. | §8.2.1, §26.5 |
| ARCVB-ARCH-03 | Layer 3 MUST execute against Layer 1 claims, not against a private copy. | §25.1 |
| ARCVB-ARCH-04 | Layer 4 MUST accept writes only from ARCVB services through an append-only interface. The ANS MUST NOT have write or delete access to the ledger. | §9.14, §26.4 |
| ARCVB-ARCH-05 | No subsystem may override a claim. A subsystem that detects a condition inconsistent with a closed or bounded claim MUST raise an escalation event, write it to the ledger and re-open the claim. | §9.14 |
| ARCVB-ARCH-06 | Every layer boundary MUST be a declared interface with a stated integrity method (§9). | §20.2, §20.3, §26.4 |

### 4.3 Integration modes

The blueprint does not say whether ARCVB sits inside or beside the ship's safety chain. That decision changes which failures matter, so it is declared per vessel.

4.3.1 **M0 — Offline.** The ARCVB core runs the harness, the claim register and the package generator. It has no runtime connection to a ship.

4.3.2 **M1 — Observer.** The ARCVB core reads ANS and sensor data at runtime, computes rule state and sufficiency state, runs the runtime monitors and writes the ledger. It sends nothing to the ANS. It sends alerts and escalation events to the ROC and the master only.

4.3.3 **M2 — Advisory.** As M1, and the ARCVB core also publishes rule state and sufficiency state to the ANS as inputs. The ANS retains decision authority and decides whether and how to use them.

4.3.4 **M3 — In-loop.** The ARCVB core's outputs gate or constrain ANS commands, for example by commanding a declared fallback state. M3 places the ARCVB core inside the safety chain.

4.3.5 This version specifies M0, M1 and M2 normatively. M3 is an open item (Annex E, ARCVB-K3) and MUST NOT be claimed under this version.

| ID | Requirement | UCFS trace |
|---|---|---|
| ARCVB-MODE-01 | The integration mode MUST be declared in the claim register and in the approval basis. | §27.8 |
| ARCVB-MODE-02 | In M2, the ARCVB core's own failure modes (§8) MUST be declared as claims, with owners, because an ANS that uses ARCVB outputs depends on them. | §8.4.1 |
| ARCVB-MODE-03 | In M1 and M2, loss of the ARCVB core MUST NOT remove or alter any ANS safety function. Loss MUST be indicated to the ROC and the master. | §24.3 |
| ARCVB-MODE-04 | Where the blueprint states that the engine "shifts the ship" to a fallback state, the actor that executes the shift MUST be named in the claim's failure-mode response. | §8.4.1, §8.10.1 |

---

## 5. Core subsystems

### 5.1 Subsystem A — Rule-state machine (UCFS domains D-A, D-B, D-D)

#### 5.1.1 Function

Subsystem A evaluates observable variables continuously and declares which rule set governs the ship's relationship to each relevant target or area. It implements the *Ever Smart* observable map (UCFS Annex B) and the rule-switching requirements of UCFS §11.

#### 5.1.2 Inputs

Radar tracks, AIS (with integrity assessment, UCFS §20.3), electronic chart (ENC) data, sensor confidence metrics from Subsystem B, PNT state (UCFS §20.2), and the declared jurisdiction and rule-set plurality (UCFS §10.6).

#### 5.1.3 States

The minimum state set is the *Ever Smart* three-situation set: **Crossing**, **Transition**, **Shaping to enter** (UCFS Annex B). Further states are declared for restricted visibility (UCFS §12.6) and for rule-set transitions at a demarcation line (UCFS §10.6).

Transition criteria are defined by the submitter as observables with thresholds, each with a derivation protocol (UCFS §8.6).

#### 5.1.4 Illustrative parameters (not thresholds)

The blueprint offered a transition rule based on a sustained course change of at least 5° over 60 seconds, entrance-axis alignment and closure rate. These three observable *classes* are retained as examples of what a threshold set can use. The figures are **not** values for any vessel. They are not derived, not validated, and MUST NOT be cited as a standard (UCFS §11.8, Annex A, A29).

#### 5.1.5 Requirements

| ID | Requirement | UCFS trace |
|---|---|---|
| ARCVB-RS-01 | Every transition between rule states MUST be defined by declared observables, a threshold with a derivation protocol, a reversion hysteresis and a verification scenario. | §8.6, §11.3, §9.4 |
| ARCVB-RS-02 | A crossing-rule engagement MUST NOT require a steady course as a precondition. The engine MUST declare the bearing-rate measurement accuracy and the observables used to detect a steady bearing. | §11.2 |
| ARCVB-RS-03 | Bearing rate, CPA, TCPA and closure rate MUST be computed with propagated uncertainty. Rule engagement and Rule 17(b) triggers MUST be evaluated against the confidence interval, not a point estimate. | §9.5, §9.5.1, §13.6 |
| ARCVB-RS-04 | The engine MUST implement separate claims and separate logic for Rule 17(a)(ii) (observational) and Rule 17(b) (predictive). | §11.5 |
| ARCVB-RS-05 | The engine MUST address a vessel already aligned and closing without a detectable course adjustment, either as a declared design question or as a bounded fallback. | §11.4 |
| ARCVB-RS-06 | The engine MUST declare maximum decision latency and the range and timing at which avoiding action begins. | §11.6, §13.5 |
| ARCVB-RS-07 | Each rule state output MUST carry a confidence band and the claim identifiers whose observables it used. | §8.11.2, §8.2.1 |
| ARCVB-RS-08 | A claim relying on *Ever Smart* MUST state that the holdings are UK law and MUST state the governing interpretation relied on in the operating jurisdiction. Where *Ever Smart* is not binding, the submitter MUST elect it or state what is relied on instead. The engine's configuration MUST record that election. | §11.1, §11.1.1 |
| ARCVB-RS-09 | The engine MUST NOT switch rule state on a timer alone or on a static boundary alone where the declared claim relies on observable intent. | §11.3, §9.4 |
| ARCVB-RS-10 | A rule state held while sensor sufficiency is *degraded* or *insufficient* MUST be flagged as low-confidence in the output and the ledger. | §12.3, §12.4 |

### 5.2 Subsystem B — Look-out and sensor-sufficiency engine (UCFS domain D-C)

#### 5.2.1 Function

Rule 5 requires a proper look-out by "sight and hearing" and by all available means. Machine perception (fusion of radar, cameras, lidar, acoustic and other sensing) has no standardized benchmark. Subsystem B evaluates whether the data are sufficient to support the claims that depend on them, and declares the result.

#### 5.2.2 Compression type

The default compression type set for the Rule 5 claim is **[application, interpretation]**, application first (UCFS §12.1.1). ARCVB MUST NOT label the function "equivalence" unless the submitter has identified a formal COLREG equivalence route (UCFS Annex K1).

#### 5.2.3 Outputs

A sufficiency state (§3.3), the sensor-suite degradation mode, the data-confidence value against the declared threshold and floor, and an escalation event to the ROC and the master on threshold breach.

#### 5.2.4 Requirements

| ID | Requirement | UCFS trace |
|---|---|---|
| ARCVB-LO-01 | The engine MUST be configured with a declared sensor-sufficiency threshold and uncertainty floor, each with a derivation protocol. The claim MUST state whether the threshold is vessel-specific or relies on a published benchmark, and MUST record that no accepted reference test was identified where that is so. | §12.3, §8.6 |
| ARCVB-LO-02 | Below the threshold the engine MUST raise an alert to the ROC and the master and MUST declare the sufficiency state. The declared degraded or fallback state MUST be named in the claim. | §3.28, §8.10.1 |
| ARCVB-LO-03 | The engine MUST map sensor functions to the elements of Rule 5: fusion for sight, acoustic sensing for hearing, data links and other sources for "all available means". The mapping MUST be recorded in the regulatory gap analysis. | §12.2 |
| ARCVB-LO-04 | The engine MUST declare its performance against small, low-signature targets, with the target set defined in the derivation protocol. It MUST NOT assume camera or fused-sensor detection is sufficient without declared performance. | §12.2, §20.4 |
| ARCVB-LO-05 | The engine MUST declare the fusion state treated as equivalent to "detects by radar alone" for Rule 19, with a derivation protocol stating which sensors are active, which are fused, and how the state corresponds to the Rule's concept. | §12.6.1, §12.6.2 |
| ARCVB-LO-06 | The engine MUST declare the sensor-sufficiency threshold and uncertainty floor for Rule 7(c) "scanty information", and MUST state that the Code gives no sensor-data threshold for "scanty". | §12.5, §13.2 |
| ARCVB-LO-07 | PNT denial, spoofing and jamming MUST be treated as a sensor-sufficiency failure that triggers the Rule 5 fallback. AIS spoofing, latency and data-quality degradation MUST reduce the sufficiency state or confidence of the observables that depend on AIS. | §20.2, §20.3 |
| ARCVB-LO-08 | Degraded states MUST declare triggers, fallback behaviour, escalation route and reversion hysteresis, and MUST be exercised by the harness. | §12.4, §9.4 |
| ARCVB-LO-09 | Look-out evidence (threshold, floor, degradation tests, target set) MUST be retained in investigator-usable form. | §12.8, §17.4 |
| ARCVB-LO-10 | The Rule 5 claim is in a non-waivable domain (UCFS NW-1). A residue is S1. A bounded claim is S2 and MUST carry a runtime monitor that escalates to the master on threshold breach. | §5.4.2, §8.10.3 |

### 5.3 Subsystem C — Responsibility and handover ledger (UCFS domains D-E, D-F)

#### 5.3.1 Function

Moving from a traditional crew to an automated ROC creates an accountability structure across Company, ship, ROC and master (the ISM quadrilateral). Subsystem C tracks which actor holds authority at each moment and records transfers.

#### 5.3.2 Authority states

ANS, ROC operator, master on board, and declared intermediate states (for example *handover requested*, *handover accepted, situation awareness rebuilding*). The state set and the allowed transitions are declared in the claim register.

#### 5.3.3 Requirements

| ID | Requirement | UCFS trace |
|---|---|---|
| ARCVB-HO-01 | The tracker MUST implement the event chain: detection → alert → operator acknowledge → situation awareness established → authority accepted → action. Evidence MUST be declared per segment and a maximum end-to-end latency MUST be declared. | §14.1 |
| ARCVB-HO-02 | The operator's situation-awareness rebuild time after handover MUST be declared with evidence and treated as a latency component. | §14.2 |
| ARCVB-HO-03 | Every handover MUST be recorded with exact timestamps, the authority transfer and the accepting actor, each with a time-service reference. | §14.4, §26.5.1 |
| ARCVB-HO-04 | The ANS fallback behaviour during the handover chain MUST be declared and logged. | §14.1 |
| ARCVB-HO-05 | The tracker MUST record ROC workload, rest-hour records and multi-ship alarm load, using vessel-specific quantification declared by the submitter. | §14.5, §14.8 |
| ARCVB-HO-06 | Where one ROC or one master covers several ships, fleet-level claims MUST be recorded with common-cause analysis and a fleet runtime monitor. | §14.8 |
| ARCVB-HO-07 | The responsibility matrix MUST be generated as a view over the claim register, from flag State to ANS, covering the ISM quadrilateral and any responsibility transferred from the ship security officer. A responsibility with no owner MUST be reported as a failure of NW-6. | §14.9, §15.5 |
| ARCVB-HO-08 | The tracker MUST record the declared limits of ANS authority. It MUST NOT represent the ANS as a legal person. | §14.9 |
| ARCVB-HO-09 | The ledger MUST NOT be described as proving due diligence or as mitigating any admiralty doctrine. Its effect on liability is for counsel. | §21.1, §21.2 |

### 5.4 Subsystem D — Version-lock and regulatory-drift mapper (UCFS domain D-I)

#### 5.4.1 Function

Software updates occur on a commercial cadence. Treaty amendments, statutes and case law change over years. Subsystem D keeps the version lock current, compares software changes against the claims they affect, and classifies each change.

#### 5.4.2 Change classes

(1) Requires re-assessment; (2) pre-approved within declared bounds; (3) administrative (UCFS §18.2).

#### 5.4.3 Requirements

| ID | Requirement | UCFS trace |
|---|---|---|
| ARCVB-DR-01 | The mapper MUST maintain the version manifest (§3.8) and MUST record, per claim, the instrument, case-law, class-notation and software versions. | §18.1 |
| ARCVB-DR-02 | The mapper MUST hold a table of adopted, accepted, in-force and applicable amendments for each instrument relied on, with defined re-open triggers. | §16.10, §18.3 |
| ARCVB-DR-03 | A software change MUST be classified (§5.4.2) before deployment. A change that alters declared vessel behaviour, a threshold, a rule-state transition criterion or a runtime monitor MUST NOT be classified as administrative. | §18.2, NW-8 |
| ARCVB-DR-04 | Class (2) changes MUST stay within bounds declared in the approval basis, with the supporting evidence. The mapper MUST state that whether an Administration will accept bounded pre-approval is unknown. | §18.2, Annex K4 |
| ARCVB-DR-05 | A change in an instrument, a case-law position or a class notation that a claim relies on MUST raise the claim's re-open trigger and an escalation event to the claim owner. | §18.3, §18.4, §18.5 |
| ARCVB-DR-06 | The mapper MUST declare how commercial-cadence software updates are handled within the change classification. | §18.6 |
| ARCVB-DR-07 | A change-control classification MUST exist before an approval basis is treated as version-locked. Absence is a failure of NW-8. | §5.4.1 (NW-8) |

---

## 6. Cross-cutting services

### 6.1 Claim register service and consistency checker (UCFS §8, §9.6)

| ID | Requirement | UCFS trace |
|---|---|---|
| ARCVB-CR-01 | The service MUST hold every claim, residue and watch item with the attributes listed in UCFS §8.2.1. A claim missing a required attribute MUST NOT be recorded as closed or bounded. | §8.2.1, §8.2.2 |
| ARCVB-CR-02 | The service MUST enforce the status–compression mapping in UCFS §8.3.10. A claim with a compression type not permitted for its status MUST NOT be recorded as that status. | §8.3.10 |
| ARCVB-CR-03 | The service MUST assign each uncertainty to exactly one domain and MUST split a cross-domain uncertainty into one claim per domain with a shared obligation reference. | §6.1 |
| ARCVB-CR-04 | The service MUST record, per claim, the provisional status of every source relied on and the route (a) or (b) by which a [P] status was cleared. | §2.2.3 |
| ARCVB-CR-05 | The service MUST record severity classes and MUST refuse a gate pass in violation of UCFS §5.3 or §5.4. A void gate MUST be flagged in the ledger. | §5.5 |
| ARCVB-CR-06 | The consistency checker MUST test claims sharing an obligation reference or a runtime resource (time, sensor, operator attention) for mutual satisfiability at every gate. | §9.6 |
| ARCVB-CR-07 | A reclassification of a domain MUST be recorded with reason and re-assessment and MUST trigger a consistency check. | §6.5 |
| ARCVB-CR-08 | The service MUST record the evidence tier of each evidence item and MUST check it against the domain minimum in UCFS §8.5.5. | §8.5.5, §17.3 |
| ARCVB-CR-09 | A bounded claim requiring an E4 obligation MUST carry the five items in UCFS §8.5.6 (data-collection plan, reporting cadence, re-assessment trigger, fallback if E4 evidence does not materialize, owner). | §8.5.6 |

### 6.2 Runtime monitor service (UCFS §24, §5.2.4)

| ID | Requirement | UCFS trace |
|---|---|---|
| ARCVB-RM-01 | Every closed or bounded claim MUST be bound to a runtime monitor. A claim without a specified, tested runtime monitor cannot close at G2. | §24.1, §5.2.4, §24.6 |
| ARCVB-RM-02 | A monitor MUST be able to detect claim violation, threshold breach, confidence-band breach and fallback-state entry. | §24.2 |
| ARCVB-RM-03 | A violation MUST raise an escalation event, write it to the ledger with timestamp and time-service reference, re-open the claim and trigger the failure-mode response declared in the claim. | §24.3 |
| ARCVB-RM-04 | Monitor evidence MUST be retained as an E4 stream. | §24.5 |
| ARCVB-RM-05 | Monitor test evidence of at least E2 MUST exist at G2 for every closed and bounded claim in scope. | §5.2.4 |
| ARCVB-RM-06 | A confidence-band breach MUST be treated as a re-open trigger. | §8.11.4 |
| ARCVB-RM-07 | A bounded claim in a non-waivable domain MUST have a monitor that escalates to the master on threshold breach. | §8.10.3 |

### 6.3 Time service (UCFS §26.5, NW-7)

| ID | Requirement | UCFS trace |
|---|---|---|
| ARCVB-TM-01 | The service MUST declare time sources and priority (for example GNSS, atomic, NTP, PTP, ship clock, ROC clock), synchronization method and frequency, drift bounds, holdover behaviour, integrity monitoring and fallback ordering. | §26.5 |
| ARCVB-TM-02 | The service MUST detect time-source denial or spoofing and MUST write the detection to the ledger. | §26.5 |
| ARCVB-TM-03 | Every ledger record, handover record and escalation event MUST carry the time value, the source identifier and a time-quality indicator. | §26.5.1, §14.4 |
| ARCVB-TM-04 | Absence of a declared time architecture and tamper-evidence method is a failure of NW-7. | §5.4.1 (NW-7) |

### 6.4 V&V harness (UCFS §25)

#### 6.4.1 Function

The harness executes every closed and bounded claim against scenarios, records the result and emits evidence in a form the ledger can retain.

#### 6.4.2 Requirements

| ID | Requirement | UCFS trace |
|---|---|---|
| ARCVB-VV-01 | The harness MUST execute every closed and bounded claim. | §25.1 |
| ARCVB-VV-02 | The harness MUST cover at minimum the scenario families in UCFS §25.2. | §25.2 |
| ARCVB-VV-03 | The harness MUST record, per scenario: the claim exercised, the acceptance criterion, the result, the evidence artifact and the evidence tier. | §25.3 |
| ARCVB-VV-04 | The harness MUST emit evidence artifacts carrying type, producer, timestamp per the time service, integrity method and custody history. | §17.6, §25.4 |
| ARCVB-VV-05 | The harness MUST NOT be presented as validated by any Administration or classification society unless it has been. | §25.5 |
| ARCVB-VV-06 | Harness results produced by the submitter or developer are E2. They MUST NOT be recorded as E3. E3 requires verification by a party independent of the developer. | §8.5.2, §8.5.3 |
| ARCVB-VV-07 | V&V results for every closed and bounded claim, with evidence tier and artifact reference, MUST be exported to the approval package at G6. | §5.2.5, §25.7, §27.9 |

#### 6.4.3 Scenario families (restated for convenience)

The families in UCFS §25.2 apply: crossing without intent to enter; shaping to enter on final approach; waiting for a pilot; give-way vessel on erratic course with steady bearing; already aligned and closing without detectable course adjustment; sensor degradation affecting bearing or closure rate; PNT denial or spoofing; AIS spoofing or latency; small low-signature targets; non-cooperative, deceptive or poorly detectable targets; restricted visibility; cyber-induced degraded states; rule-set transition at a demarcation line; handover under maximum declared latency including SA-rebuild; fleet-level multi-ship alarm load; degraded-state reversion hysteresis; communications failure and distress response; anchoring, mooring, pilotage and tug scenarios where applicable. UCFS governs if this list and UCFS §25.2 differ.

### 6.5 Audit ledger (UCFS §26)

#### 6.5.1 Function

The ledger records claims, evidence, escalation events, handovers, rule-state and sufficiency-state changes and ledger administration, in a tamper-evident, investigator-usable form.

#### 6.5.2 Requirements

| ID | Requirement | UCFS trace |
|---|---|---|
| ARCVB-AL-01 | The ledger MUST record every claim, its status, evidence, tier, owner, version lock, severity class and re-open trigger. | §26.1 |
| ARCVB-AL-02 | The ledger MUST record handover timestamps, authority transfers, SA-rebuild segments, escalation events, degraded-state transitions and PNT and time integrity events. | §26.2 |
| ARCVB-AL-03 | The ledger MUST record the custody and access history of every evidence artifact. | §26.3 |
| ARCVB-AL-04 | The ledger MUST declare its integrity method: hash chain, signed append-only log, external timestamping, or a declared combination. "Tamper-evident" alone is not a method. | §26.4 |
| ARCVB-AL-05 | The ledger MUST record the hash algorithm, the signing keys and their custody, the timestamping method and the audit trail of ledger administration. | §26.6 |
| ARCVB-AL-06 | The ledger MUST be available to the Administration and investigators on request, subject to the declared privilege posture. | §26.7 |
| ARCVB-AL-07 | The submitter MUST declare, per jurisdiction: fields produced on request; safety-management records and their production basis; privileged risk assessments and legal memoranda; the legal-hold procedure; and counsel sign-off meeting the criterion in UCFS §26.8.3. | §26.8 |
| ARCVB-AL-08 | The ledger MUST be investigator-usable. It MUST claim integrity and usability and MUST NOT claim court admissibility. | §21.3 |
| ARCVB-AL-09 | The ledger MUST support legal hold and post-casualty preservation. | §21.4 |
| ARCVB-AL-10 | ARCVB MUST NOT assume the ledger is costless to create or uniformly producible. The disclosure posture is itself a claim with an owner, acceptance criterion and re-open trigger. | §26.8.1 |
| ARCVB-AL-11 | A gate decision (pass or fail), the residues in scope and their severity classes MUST be recorded in the ledger. | §5.2.3 |

### 6.6 Package generator (UCFS §27)

| ID | Requirement | UCFS trace |
|---|---|---|
| ARCVB-PK-01 | The approval basis MUST be generated as a view over the claim register, not as a separate document with duplicated logic. | §27.1 |
| ARCVB-PK-02 | The generator MUST produce, as views: the claim register, the responsibility matrix, the annexes, the certificate and document register, the PSC approval passport, the disclosure and privilege statement and the time architecture. | §27.4, §19.3, §19.4 |
| ARCVB-PK-03 | The package MUST contain the ConOps identifying possible deviations from applicable rules and justifying alternative solutions on the basis of risk assessment. | §27.2 |
| ARCVB-PK-04 | The package MUST distinguish interpretation from departure. | §27.5, §8.7 |
| ARCVB-PK-05 | The package MUST declare its conformance vector, its conformance claim and the version lock. | §27.8 |
| ARCVB-PK-06 | The package MUST state that its force comes from the Administration's approval and national implementation, not from the non-mandatory Code. | §27.6 |
| ARCVB-PK-07 | The package MUST include V&V results (ARCVB-VV-07). | §27.9 |
| ARCVB-PK-08 | The package MUST NOT use the phrase "UCFS-conformant" or any derivative while UCFS Annex I is unpopulated. | §28.6.1, §28.6.2 |
| ARCVB-PK-09 | The package MUST declare the approval withdrawal, suspension and condition-change procedure. | §19.5 |
| ARCVB-PK-10 | The generator MUST NOT state or imply that the package is "IMO-compliant", approved or certified. | §1.4.4 |

### 6.7 Approval-basis schema

6.7.1 The blueprint proposes a standardized JSON/YAML schema for the vessel ConOps and regulatory gap analysis. ARCVB adopts the idea as a requirement for a **versioned, machine-readable schema** derived from the UCFS claim model.

| ID | Requirement | UCFS trace |
|---|---|---|
| ARCVB-SC-01 | The schema MUST be derived from UCFS §8.2.1 so that every UCFS claim attribute has a field. A change to UCFS §8.2.1 MUST produce a new schema version. | §8.2.1, §28.4 |
| ARCVB-SC-02 | The schema MUST be versioned and the schema version MUST be part of the version lock. | §18.1 |
| ARCVB-SC-03 | The schema MUST encode the compression type as an ordered set and the status as a separate field, and MUST validate them against the mapping in UCFS §8.3.10. | §8.3.10 |
| ARCVB-SC-04 | The schema MUST carry the [P] flag and clearing route per source. | §2.2.3 |
| ARCVB-SC-05 | An illustrative record is given in Annex C. It is not a validated schema. | — |

---

## 7. Interfaces

7.1 Interfaces are listed in Annex D. Every interface MUST have a declared owner, data format, rate, integrity method and failure behaviour.

| ID | Requirement | UCFS trace |
|---|---|---|
| ARCVB-IF-01 | Every input MUST carry a quality or confidence indicator, or ARCVB MUST assign a declared default and record that it did. | §9.5 |
| ARCVB-IF-02 | Loss of an input MUST change the sufficiency state or the confidence of dependent outputs. It MUST NOT be silently ignored. | §12.4 |
| ARCVB-IF-03 | The ARCVB core MUST authenticate its configuration and its software. A configuration or software change MUST pass Subsystem D before deployment. | §18.2, §20.1 |
| ARCVB-IF-04 | Cyber risk assessment for the ARCVB core SHOULD be connected to COLREG-critical functions. Cyber-induced degraded states and their fallback and escalation routes MUST be declared where the submitter elects the linkage. | §20.1 |
| ARCVB-IF-05 | Communications failure (including loss of the control link) MUST be handled as a declared failure mode with fallback. | §22.4 |

---

## 8. Safety and failure behaviour of ARCVB itself

8.1 In M1 and M2 the ARCVB core is a source of alerts and, in M2, of inputs to the ANS. Its failure modes therefore matter. The blueprint does not address them.

8.2 The following failure modes MUST be declared as claims, with detection, response and owner, for every deployment:

| # | Failure mode | Minimum declared response |
|---|---|---|
| 8.2.1 | ARCVB core process failure | Indicate to ROC and master; ANS safety functions unaffected (ARCVB-MODE-03); record in the ledger when able |
| 8.2.2 | Ledger write failure | Buffer within declared bounds; alert; declare the ledger gap; the gap is itself a ledger event once writing resumes |
| 8.2.3 | Time-source denial or spoofing | Fall back per the declared time architecture; flag affected records; alert (ARCVB-TM-02) |
| 8.2.4 | Input loss or degraded data quality | Lower sufficiency state or confidence (ARCVB-IF-02); alert |
| 8.2.5 | Configuration or software corruption | Detect by authentication failure; refuse to start in an unauthenticated state; alert |
| 8.2.6 | Rule-state machine fault or oscillation | Declared hysteresis (ARCVB-RS-01); declared low-confidence output (ARCVB-RS-10); escalation |
| 8.2.7 | Monitor failure (a monitor that stops reporting) | A missing monitor heartbeat MUST itself raise an escalation event |
| 8.2.8 | Disagreement between ARCVB state and ANS state | Escalation event; claim re-opened; no subsystem overrides a claim (ARCVB-ARCH-05) |
| 8.2.9 | Link loss to the ROC | Declared fallback; record when able (ARCVB-IF-05) |

8.3 ARCVB MUST NOT suppress an alert in order to avoid operator alarm load. Alarm load is a ROC workload claim (ARCVB-HO-05), not a reason to hide an escalation event.

---

## 9. Conformance of an ARCVB implementation

9.1 An ARCVB implementation MAY state which requirements in this specification it implements. That statement is a measurement and is not a conformance claim under UCFS (UCFS §4.1.3).

9.2 A deployment that claims UCFS conformance MUST state its vector (UCFS §4.2) and satisfy the gates (UCFS §5). It MUST NOT use "UCFS-conformant" while UCFS Annex I is unpopulated.

9.3 **Bridge claim.** UCFS §24.4 says the runtime monitors are the operational bridge between UCFS and ARCVB. UCFS §24.4.1 records that as a proposed claim and open item K2: whether the ARCVB implementation actually performs the bridge is not verified.

9.3.1 The following acceptance criteria are proposed for closing K2 for a reference vessel register. They are a design choice and are not part of UCFS.

- (a) Every closed and bounded claim in the reference vessel register is bound to a runtime monitor (ARCVB-RM-01).
- (b) The harness fires each monitor with an injected violation, and the escalation event, ledger record and claim re-open are observed (ARCVB-RM-03, ARCVB-VV-01).
- (c) The monitor test evidence is reviewed by a party independent of the developer, so that the result is E3 rather than E2.
- (d) A missing-heartbeat test (8.2.7) is included.

9.3.2 Until (a)–(d) are satisfied, the bridge claim remains **[P] — proposed**.

9.4 The framework and this specification were developed with an AI collaborator and have not been independently reviewed. Under UCFS §25.3-type reasoning, development by the same collaborator is development evidence, not independent corroboration. An independent review is the step that would strengthen any claim made about ARCVB.

---

## 10. Openness and adoption (replaces blueprint §4, "viral")

10.1 The blueprint proposed releasing an open reference implementation first, standardizing the approval-basis schema, and targeting the dual-use market. The intent, to make the work usable and testable by others, is kept. The "viral" framing, the adoption forecast ("adoption explodes") and the time claim are not.

10.2 **Open items already recorded in UCFS.** UCFS did not adopt opening the harness before the claim model is stable (UCFS §0.2.4). Openness is conditional on a conformance-mark policy (UCFS §28.6, Annex I). The reference protocol library governance and the antitrust and confidentiality posture for shared precedent are open (UCFS Annex K9, K10).

10.3 **Proposed sequence** (design choice, not a commitment):

| Step | Content | Precondition |
|---|---|---|
| 1 | Publish the claim-record schema (§6.7) as a versioned draft with the illustrative record in Annex C | The UCFS §8.2.1 attribute list is stable at the published version |
| 2 | Run the harness against a reference vessel register (not an operational vessel) and publish the results as E2 | The reference vessel register exists; [P] flags are carried |
| 3 | Seek independent review of the monitor bridge (§9.3.1) | Step 2 complete |
| 4 | Release the harness as an open developer kit | UCFS Annex I populated; claim model stable; confidentiality posture decided (UCFS K10) |

10.4 **Audiences.** UCFS Annex G governs. Dual-use targeting (vessel program offices and commercial autonomy developers) is a business choice outside this specification. Warships and government non-commercial ships are outside the MASS Code; civil-military encounter conduct is an external watch item (UCFS Annex H7) and a scenario input to the harness, not a claim.

10.5 ARCVB MUST NOT be described to any audience as producing an approval, a certificate, a compliant package or a legal defence.

---

## Annex A — Blueprint-to-specification map

| Blueprint section | Where it went |
|---|---|
| 1. Executive summary and core mission | §1 (purpose and limits); §0.1.1–0.1.3 (changed claims) |
| 2. Four architectural layers | §4.1, §4.2 |
| 3A. Dynamic rule-switching state machine | §5.1 |
| 3B. Look-out equivalence and sensor-sufficiency engine | §5.2 (renamed; §0.1.8) |
| 3C. Responsibility and handover ledger | §5.3; ledger function in §6.5 |
| 3D. Version-locking and drift mapper | §5.4 |
| 4. Implementation strategy ("viral") | §10 |
| *(not in blueprint)* | Integration modes §4.3; claim register §6.1; runtime monitors §6.2; time service §6.3; harness requirements §6.4; ledger requirements §6.5; package generator §6.6; schema §6.7; interfaces §7; ARCVB failure behaviour §8; K2 criteria §9.3 |

---

## Annex B — Traceability matrix (ARCVB component → UCFS)

| ARCVB component | UCFS clauses implemented | UCFS domains | Gates supported |
|---|---|---|---|
| Layer 1 — claim register service (§6.1) | §6, §8.1–8.11, §9.6, §2.2 | all | G0, G1 |
| Subsystem A — rule-state machine (§5.1) | §11, §13.6, §9.4, §9.5, Annex B | D-A, D-B, D-D | G2 |
| Subsystem B — look-out and sufficiency (§5.2) | §12, §20.2–20.4, §8.10 | D-C, D-K | G2 |
| Subsystem C — handover and responsibility (§5.3) | §14, §15.5, §21.1 | D-E, D-F, D-L | G3 |
| Subsystem D — drift mapper (§5.4) | §16.10, §18 | D-I | G4 |
| Runtime monitor service (§6.2) | §24, §5.2.4, §8.11.4 | all closed and bounded claims | G2 |
| Time service (§6.3) | §26.5, NW-7 | D-H | G5 |
| V&V harness (§6.4) | §25, §5.2.5 | all | G2, G6 |
| Audit ledger (§6.5) | §26, §21.3, §21.4, NW-7 | D-H, D-L | G5 |
| Package generator (§6.6) | §27, §19.3–19.5 | D-J, D-H | G6 |
| Schema (§6.7) | §8.2.1, §8.3.10, §28.4 | all | G1, G6 |

Non-waivable domains touched by ARCVB: NW-1 (Subsystem B), NW-2 (Subsystem A, Rule 17(b)), NW-6 (Subsystem C), NW-7 (time service, ledger), NW-8 (Subsystem D). NW-3 (statutory complement), NW-4 (MARPOL Annex I) and NW-5 (ISM/ISPS interfaces) are not implemented by an ARCVB component and remain the submitter's to claim in the register.

---

## Annex C — Illustrative records (not a validated schema)

All values are placeholders. `TBD` marks something the submitter must supply. Nothing here is a threshold, an evidence result or a claim about any vessel.

### C.1 Claim record

```yaml
schema_version: "arcvb-claim-0.1-draft"
claim_id: "CLM-EXAMPLE-0001"
obligation_ref: "COLREG Rule 5 (look-out)"
domain: "D-C"
sub_item: "D-C.2"                      # degraded states and sensor-sufficiency threshold
jurisdiction: "TBD"
compression_type_set: ["bounded fallback"]   # UCFS 8.3.10: bounded status -> bounded fallback
status: "bounded"
evidence_tier_minimum: "E2 + E4 obligation"  # UCFS 8.5.5, D-C.2
contestation_level: "novel"            # no accepted benchmark identified
confidence_band:
  range: "TBD"
  derivation_protocol_ref: "DP-EXAMPLE-0001"
observable: "fused data-confidence value for look-out"
threshold_or_bound:
  threshold: "TBD"                     # vessel-specific; derivation protocol required
  uncertainty_floor: "TBD"
  hysteresis: "TBD"
fallback_state: "TBD (named degraded state)"
escalation_route: "alert to ROC and master"
derivation_protocol_ref: "DP-EXAMPLE-0001"
uncertainty_propagation_ref: "UP-EXAMPLE-0001"
acceptance_criterion: "TBD"
evidence_items:
  - id: "EV-EXAMPLE-0001"
    tier: "E2"
    timing: "before approval decision"
    artifact_ref: "TBD"
owner: "TBD"
version_lock:
  instruments: "TBD"
  case_law: "TBD"
  class_notation: "TBD"
  software: "TBD"
  schema: "arcvb-claim-0.1-draft"
failure_mode:
  mode: "sensor data confidence falls below threshold"
  detection: "sufficiency evaluation (Subsystem B)"
  response: "escalation event; ANS enters declared fallback state"
  actor_executing_fallback: "ANS"      # integration mode M2; see ARCVB-MODE-04
runtime_monitor:
  monitor_id: "RM-EXAMPLE-0001"
  escalates_to: "master"               # required for bounded claims in non-waivable domains
reopen_trigger: "confidence-band breach; sensor suite change; threshold change"
severity_class: "S2"                   # bounded claim in non-waivable domain (NW-1)
e4_obligation:                         # UCFS 8.5.6
  data_collection_plan: "TBD"
  reporting_cadence: "TBD"
  reassessment_trigger: "TBD"
  fallback_if_no_e4: "TBD"
  owner: "TBD"
provisional_sources:
  - source: "TBD"
    status: "TBD"
    clearing_route: "TBD"
```

### C.2 Ledger record

```yaml
schema_version: "arcvb-ledger-0.1-draft"
sequence: 0
time:
  value: "TBD (UTC)"
  source_id: "TBD"
  quality: "TBD"
event_type: "escalation | handover | rule_state_change | sufficiency_change | gate_decision | config_change | evidence_added | ledger_admin"
claim_id: "CLM-EXAMPLE-0001"
payload_hash: "TBD"
previous_record_hash: "TBD"
signature:
  key_id: "TBD"
  algorithm: "TBD"
```

### C.3 Rule-state record

```yaml
schema_version: "arcvb-rulestate-0.1-draft"
target_ref: "TBD"
rule_state: "Crossing | Transition | Shaping to enter | TBD"
confidence_band: "TBD"
sufficiency_state: "sufficient | degraded | insufficient"
low_confidence_flag: false
governing_interpretation: "TBD"        # UCFS 11.1 election recorded in configuration
claims_used: ["CLM-EXAMPLE-0001"]
time_ref: "TBD"
```

---

## Annex D — Interface list

| # | Interface | Direction | Content | Required declared properties |
|---|---|---|---|---|
| D1 | Radar | in | Tracks and quality | Owner, rate, integrity, loss behaviour |
| D2 | AIS | in | Reports; integrity assessment | Spoofing and latency handling (UCFS §20.3) |
| D3 | Electronic chart (ENC) | in | Chart data and version | Version in the version manifest |
| D4 | Other perception sensors | in | Camera, lidar, acoustic, others, with confidence | Fusion state mapping (ARCVB-LO-05) |
| D5 | PNT | in | Position, velocity, time, integrity flags | Denial and spoofing handling (UCFS §20.2) |
| D6 | ANS state | in | Mode, authority state, commanded actions | Used for ARCVB-ARCH-05 and 8.2.8 |
| D7 | ROC events | in | Operator acknowledge, acceptance, workload and rest records | Time-service reference |
| D8 | Version manifest | in | Software, schema, instrument and case-law versions | Authentication (ARCVB-IF-03) |
| D9 | Alerts and escalation events | out | To ROC and master | Delivery confirmation or declared loss behaviour |
| D10 | Rule state and sufficiency state | out (M2 only) | To ANS | Advisory only; ANS retains authority (§4.3.3) |
| D11 | Ledger interface | out | Append-only writes; read access for Administration and investigators | Privilege posture (ARCVB-AL-07) |
| D12 | Package export | out | Approval basis views, schema records, V&V results | Version lock |

---

## Annex E — Open items (ARCVB v0.1)

These are not fixed by this specification. They are recorded so that the specification does not appear to answer them.

| # | Open item | Why it is open | Owner |
|---|---|---|---|
| ARCVB-K1 | Whether any COLREG equivalence route exists for Rule 5 | Inherited from UCFS K1; a legal question | Submitter + counsel; flag State |
| ARCVB-K2 | Whether an ARCVB implementation performs the runtime bridge | Inherited from UCFS K2; §9.3.1 proposes closure criteria | ARCVB implementer; independent reviewer |
| ARCVB-K3 | Integration mode M3 (in-loop) | Places ARCVB in the safety chain; needs its own failure analysis, evidence tiers and approval view | Author |
| ARCVB-K4 | Determinism scope in practice | §3.4 states a scope; whether the scope can be proved for a given implementation (including numerical reproducibility across hardware) is not examined | ARCVB implementer |
| ARCVB-K5 | Ledger integrity method selection | §6.5 requires a declared method but does not choose one | Submitter |
| ARCVB-K6 | Retention period and custody for evidence and ledger | Not stated in UCFS; jurisdiction-dependent | Submitter + counsel |
| ARCVB-K7 | Schema governance (who may change it, version cadence) | Related to UCFS K9 and §28.4–28.5 | Author |
| ARCVB-K8 | Independent verifier for E3 evidence | No accredited route identified | Class societies; Administrations |
| ARCVB-K9 | Whether the illustrative observable classes in §5.1.4 are adequate for any vessel | Not derived or validated | Submitter |
| ARCVB-K10 | ROC human-factors evidence for the handover chain | Evidence to be produced per vessel | Submitter + ROC |
| ARCVB-K11 | Inherited open items | UCFS K3–K12 apply to ARCVB deployments | Per UCFS Annex K |

---

## Annex F — Lineage and limits

**F1.** This specification was derived from the informal blueprint, with UCFS v0.3 as the governing parent. The disposition of each blueprint statement is recorded in §0.1.

**F2.** No requirement in this specification has been tested against a running implementation. The requirement IDs are written so that a test assertion can be derived for each one; the assertions themselves are not written here.

**F3.** The author's own comparison is the only comparison performed. It is not independent verification.

**F4.** Every UCFS cross-reference was written against the UCFS v0.3 text as merged on 14 November 2026. A change to UCFS clause numbers requires this specification to be re-traced.

---

*End of ARCVB v0.1.*
