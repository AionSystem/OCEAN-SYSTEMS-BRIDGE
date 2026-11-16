# MASS Regulatory Bridge

**Autonomous surface ships under existing and emerging rules**

*Working paper | Draft for technical review*

*Not an IMO instrument. Not legal advice. Not a certification basis.*

## The IMO MASS Code and the Legacy Regulatory Framework

**Friction Points, Case Law and Practical Implications for the Approval of Autonomous Surface Ships**

| | |
|---|---|
| Document type | Working paper, draft for technical review |
| Date | 13 November 2026 (corrected version, 14 November 2026) |
| Author and affiliation | [to be inserted] |
| Status | Not peer reviewed. Verification status of each source is stated in section 7. |

**Notices.** This paper is analysis, not authority. It is not an IMO instrument, not a flag-State circular, not a classification-society rule, and not a basis for certification. It is not legal advice; points of law, in particular those concerning liability, should be put to qualified counsel in the relevant jurisdiction. It has not been peer reviewed or endorsed by any Administration, recognized organization or industry body. Statements of what an approach "should" include are recommendations for discussion, not obligations. Section 7 states what has been checked against primary text and what has not.

## Contents

1. Executive Summary
2. Scope, Authority and Limitations
   - 2.1 Purpose and audience
   - 2.2 Status of the MASS Code
   - 2.3 The legal baseline during the transition
   - 2.4 Terms and conventions
   - 2.5 Principal limitations
3. Core Friction Analysis
   - 3.1 How to read this section
   - 3.2 COLREG
   - 3.3 SOLAS, ISM, ISPS and STCW
   - 3.4 MARPOL
   - 3.5 Other instruments and cross-cutting issues
   - 3.6 Responsibility allocation
   - 3.7 National law and regulator practice
   - 3.8 Lessons from audited naval autonomy programmes (analogy only)
4. Case Law: Evergreen Marine (UK) Ltd v Nautical Challenge Ltd [2021] UKSC 6 (*Ever Smart*)
   - 4.1 Why the case matters for autonomous ships
   - 4.2 Holdings relevant to ANS design
   - 4.3 Design and verification implications
   - 4.4 Illustrative design logic for rule switching
   - 4.5 Limits of the analysis
5. Operational and Design Implications: Using the ConOps and Approval Basis
   - 5.1 The interpretation layer the Code already contemplates
   - 5.2 What the ConOps and approval basis should state
   - 5.3 Acceptance criteria and timing of evidence
   - 5.4 Change control
   - 5.5 Considerations by audience
6. Transition Considerations, 2026–2032
7. Open Issues and Verification Needs
   - 7.1 Verification status
   - 7.2 Open substantive questions
8. Glossary
9. Sources

Appendix A. Illustrative Parameters for the Rule-Switching Logic in Section 4.4

---

## 1. Executive Summary

This paper examines where the IMO Code for Maritime Autonomous Surface Ships (MSC.595(111), the "MASS Code") meets the mandatory framework that existed before it: COLREG, SOLAS, MARPOL, STCW, the ISM and ISPS Codes, and national law. It draws on the Code, the IMO scoping work that preceded it, the *Ever Smart* judgment of the UK Supreme Court, and three reports of the US Government Accountability Office (GAO) together with later public material from the US Coast Guard.

**Principal findings**

1. **The MASS Code is guidance for now.** It was adopted on 21 May 2026, invites Governments to give effect to it from 1 July 2026, and is non-mandatory. A mandatory code is planned through a new SOLAS chapter, with entry into force no earlier than 1 January 2032 and a timeline that IMO itself says may need revisiting. Until then SOLAS, COLREG, MARPOL, STCW and national law remain the binding baseline. Compliance with the Code does not by itself relieve a ship of any mandatory requirement.

2. **Most friction is about interpretation and evidence, not about missing text.** The Code does not rewrite the legacy instruments. It asks the Administration to approve a vessel-specific concept of operations (ConOps) and approval basis that explain how an autonomous navigation system (ANS), a remote operations centre (ROC) and a remote or absent master meet provisions written for people on board. The practical question for each ship is whether that explanation is specific, testable and accepted.

3. **COLREG is the sharpest point of friction.** Rules 2, 5, 6, 7, 8, 17 and 19 and Parts C and D all assume human perception, judgment or action. IMO's 2021 scoping exercise left room for amendment; in 2023 the Maritime Safety Committee noted that COLREG requirements remain relevant and applicable regardless of how a ship is operated, and that there was no need to amend COLREG to accommodate MASS at this stage. COLREG was last amended in 2013. For the 2026–2032 transition, harmonization will therefore occur through interpretation, not amendment.

4. ***Ever Smart* supplies rare, sensor-observable tests.** The UK Supreme Court held that the crossing rules are displaced by the narrow-channel rule only when the approaching vessel is shaping to enter on final approach, not merely intending to enter; that crossing rules engage on a steady bearing, not a steady course; that Rule 17 sets out two circumstances in which the stand-on vessel's duty to keep course and speed ends (para 61), which this paper reads as an observation problem and a prediction problem; and that avoiding action must be early and readily apparent. These are UK-law holdings with persuasive weight elsewhere. They translate directly into design and verification requirements for an ANS.

5. **Several gaps concern verification rather than applicability.** COLREG Parts C and D apply unchanged, but the Code does not say who or what activates sound signals on a crewless ship or how they are surveyed. MARPOL applies, but the Code has no annex-by-annex mapping. Rule 5 equivalence has no accepted reference test. ROC rest-hour and workload implementation is unquantified.

6. **Responsibility runs through five parties under five different instruments:** flag State, Company, ROC, master and ANS. Gaps at the integrating role are the recurring failure pattern in audited autonomy programmes and should be checked for explicitly.

7. **National law is an under-mapped layer.** In the United States, statutes fix minimum complements and credentials for many vessels, and the Coast Guard has stated that it cannot waive them for autonomous vessels outside one narrow pilot authority. A MASS can satisfy the Code's equivalence test and still need the statutory complement. Other flag States' position has not been surveyed here.

8. **Evidence built for approval is also evidence in disputes.** In US admiralty law a collision involving breach of a collision rule can carry a presumption of fault. Look-out equivalence evidence, verification records and data logs should be retained in a form that investigators and counsel can use.

9. **Regulator practice is currently project-by-project.** The Coast Guard approves autonomous operations case by case; its June 2026 work instruction asks operators for a ConOps that includes a COLREGS compliance statement. Canada, the United Kingdom and Norway use small-vessel policies, exemptions and equivalences. No regulator reviewed here reports an accepted reference test for look-out equivalence.

10. **Software changes faster than approvals.** A version-locked approval basis meets software updated on a commercial cadence. Approval bases should declare which changes need re-assessment and which are pre-approved within stated bounds.

**Recommended approach in brief.** A submitter should (a) state the jurisdiction and the interpretation of each contested rule it relies on; (b) use the ConOps and approval basis as the explicit place where each friction is resolved, with thresholds, acceptance criteria and the timing of supporting evidence; (c) maintain a responsibility matrix covering flag State to ANS; (d) declare the statutory complement the flag State requires; (e) retain verification evidence; and (f) declare a change-control classification. Section 5 sets these out.

---

## 2. Scope, Authority and Limitations

### 2.1 Purpose and audience

The paper is written for practitioners who already work with these instruments: Administrations, recognized organizations, designers, operators, ROC providers and autonomy programme staff. It does not introduce the instruments; it examines the joints between them.

### 2.2 Status of the MASS Code

- The Code was adopted by resolution MSC.595(111) at the 111th session of the Maritime Safety Committee (13–22 May 2026); the resolution text records the date of adoption as 21 May 2026. Governments are invited to give effect to it from 1 July 2026. It is expressly non-mandatory.
- A roadmap contemplates a mandatory code made binding through a new SOLAS chapter. IMO-side summaries give 1 January 2032 as the earliest entry into force and state that the timeline may need revisiting. The Committee planned at its December 2026 session to re-establish a working group to frame an experience-building phase.
- The Code applies to cargo ships of 500 gross tonnage and over to which SOLAS applies, including associated ROCs, when the Administration considers compliance with the other applicable instruments impracticable or insufficient. It excludes cargo high-speed craft covered by SOLAS chapter X, warships, naval auxiliaries and other government non-commercial ships. The resolution invites application to MASS below 500 gross tonnage as far as practicable; that creates no mandatory regime for small craft.
- The Code is supplementary to SOLAS and other instruments. It does not displace them.

### 2.3 The legal baseline during the transition

Between now and entry into force of any mandatory code, the binding requirements are those of SOLAS, COLREG, MARPOL, STCW, the ISM and ISPS Codes and other conventions as applicable, together with flag-, coastal- and port-State law. The Code functions as guidance unless a State makes it binding by national implementation or other legal action. Wherever this paper says the Code "expects" or "requires" something, read it as guidance in that sense.

### 2.4 Terms and conventions

- Degrees of autonomy follow IMO's scoping exercise: degree one (automated processes and decision support, seafarers on board); degree two (remotely controlled with seafarers on board); degree three (remotely controlled without seafarers on board); degree four (fully autonomous). A ship may operate at more than one degree during a voyage.
- ANS means the autonomous navigation system; ROC the remote operations centre; ConOps the concept of operations; OE the operational envelope within which the ship is designed to operate; approval basis the vessel-specific document submitted to and approved by the Administration under the Code's approval process.
- MASS Code paragraph numbers are given for orientation and should be checked against the adopted text before citation (section 7).

### 2.5 Principal limitations

- The paper does not treat the interaction of the Code with every convention in depth; the SOLAS, MARPOL and STCW treatment is at the level of principle.
- Evidence on regulator practice is concentrated on the United States, with shorter treatment of Canada, the United Kingdom and Norway. Japan and South Korea did not respond to the audit body whose report is the main source on foreign practice. It should not be generalized to other flag States.
- The GAO reports on naval programmes are used as evidence of institutional friction, by analogy. Military acquisition is not international regulation.
- The *Ever Smart* analysis is of UK law. The design illustration in section 4 and Appendix A has not been validated by any Administration or classification society.

---

## 3. Core Friction Analysis

### 3.1 How to read this section

Each item sets out the legacy requirement, how the MASS Code treats it, the nature of the friction, and the recommended approach. "Resolved in principle" means the Code points to a route but the detail must still be shown for each ship. "Open" means neither the Code nor any source reviewed supplies an answer.

### 3.2 COLREG

**Rule 5 — look-out.**

*Requirement.* Every vessel must at all times maintain a proper look-out by sight and hearing as well as by all available means appropriate in the prevailing circumstances and conditions, so as to make a full appraisal of the situation and of the risk of collision.

*Code treatment.* The ANS is to maintain adequate situational awareness, defined as perception, comprehension and projection, and to monitor continuously the information needed for safe navigation within the OE (chapter 16).

*Friction.* "Sight and hearing" are human modalities; an ANS fuses radar, electro-optical and infrared imaging, AIS, lidar and acoustic sensing. The Rule's text does not mention sensors and has not changed. The Code does not say what demonstrates that machine perception is a "proper look-out". The US Coast Guard told GAO in 2024 that it has seen no examples of autonomous look-out technology to evaluate, that compliance with the collision regulations is therefore not established, and that IMO has determined the look-out requirement applies without amending the Regulations.

*Recommended approach.* Treat equivalence as the submitter's burden. Declare the sensor suite and its degradation modes; map functions to the Rule's elements (sensor fusion for sight, acoustic sensing for hearing, data links and other sources for "all available means"); and demonstrate the mapping in the regulatory gap analysis, including performance against small, low-signature targets (a shipbuilder cited a kayaker in a harbour as a case cameras may miss). Do not state or imply that the Rule's text has changed. Retain the evidence (section 3.7).

**Rule 2 — responsibility and departure from the Rules.**

*Requirement.* Rule 2(a) leaves the vessel, her owner, master or crew answerable for neglect of the Rules or of precautions required by the ordinary practice of seamen. Rule 2(b) requires due regard to all dangers of navigation and collision and to special circumstances, including the limitations of the vessels involved, which may justify a departure from the Rules to avoid immediate danger.

*Code treatment.* The master remains responsible for safe operation at all times and may be on board or at a ROC; if persons are on board the master is expected to be on board. Crew and remote operators must always be able and prepared to take over autonomous functions.

*Friction.* The "immediate danger" judgment may be made remotely, with communication latency. The Code specifies no maximum latency. Rule 2(b) applies to a MASS without substitution: the limitations of the vessel include those of its sensors, ANS, manoeuvring and control link.

*Recommended approach.* Declare the maximum interval from danger detection to master intervention, the ANS fallback behaviour for that interval, and how authority transfers. Treat the limits of the ANS and link as Rule 2(b) limitations in the risk assessment. A human-system limitation analysis for remote operators is good practice as a supplement to, not a replacement for, Rule 2(b).

**Rule 6 — safe speed.**

*Requirement.* Safe speed at all times, weighing visibility, traffic density, manoeuvrability, background light, wind, sea and current, draught and (with radar) the characteristics and limits of radar.

*Code treatment.* The OE records environmental limitations; the ANS must retain functionality within the OE, with degraded states and fallback outside it.

*Friction.* Rule 6 is a continuous judgment; an OE is a boundary. Leaving the OE becomes a cliff rather than a gradient.

*Recommended approach.* Express the Rule 6 factors as monitored OE parameters with margins, and define degraded-state buffers before the boundary so that behaviour does not change abruptly at the limit.

**Rule 7(c) — assumptions on scanty information.**

*Requirement.* Assumptions are not to be made on scanty information, especially scanty radar information.

*Code treatment.* The ANS must analyse and project continuously and base avoidance on risk assessment, and must alert the master as specified.

*Friction.* An ANS may have to act on degraded or incomplete data; "scanty" has no sensor-data threshold in the Code.

*Recommended approach.* Declare a sensor-sufficiency threshold and uncertainty floor below which the ANS alerts the master and enters a degraded or fallback state. Whether IMO will adopt a general threshold is unknown.

**Rule 8 — action to avoid collision.**

*Requirement.* Action must be positive, made in ample time and large enough to be readily apparent to another vessel observing visually or by radar; a succession of small alterations is to be avoided.

*Code treatment.* The ANS must be able to act in accordance with COLREG and take timely decisions within safe limits.

*Friction.* The other vessel may be conventional or itself a MASS; small incremental manoeuvres may be unreadable to either. The Code does not say how ANS actions are made readily apparent. *Ever Smart* adds a timing dimension: the manoeuvre must be taken at a time when the decision is not rushed or made on inadequate information (section 4).

*Recommended approach.* Validate legibility of manoeuvres to human visual and radar observers and, separately, to other MASS sensors. Declare maximum decision latency and the range and timing at which avoiding action begins. Digital signalling may supplement, but does not replace, the physical signals and manoeuvre legibility the Rule contemplates.

**Rules 9 and 10 — narrow channels, traffic separation, and small MASS.**

*Requirement.* Specific conduct in narrow channels and traffic separation schemes, including that vessels under 20 metres and sailing vessels shall not impede the safe passage of a power-driven vessel following a lane.

*Code treatment.* The ANS executes the voyage plan within allowable deviation. Small MASS (below 500 gross tonnage) are only invited to apply the Code.

*Friction.* A small MASS entering a separation scheme is bound by Rule 10 but may fall outside the Code. No IMO-level small-MASS regime exists. National practice is emerging (section 3.7).

*Recommended approach.* Declare the rule set applied, the behaviour in separation schemes and narrow channels, and any national small-vessel measures relied on. Where the voyage crosses a demarcation between international and inland rules (for example in US waters), declare the rule set by phase and geography and test the transition.

**Rule 17 — action by the stand-on vessel.**

*Requirement.* Under 17(a)(ii) the stand-on vessel may act by her own manoeuvre as soon as it becomes apparent that the give-way vessel is not taking appropriate action. Under 17(b), when collision cannot be avoided by the give-way vessel alone, the stand-on vessel shall take the action that best aids avoidance.

*Friction.* The two triggers are different problems. "Becomes apparent" is an observation problem: is the give-way vessel's behaviour departing from what compliance would produce? "Cannot be avoided by the give-way vessel alone" is a prediction problem: can she, from here, avoid collision alone? The Code requires projection but sets no accuracy requirement. The judgment (para 61) describes both circumstances but does not characterise them as observational and predictive. That distinction is this paper's engineering reading.

*Recommended approach.* Declare the two thresholds separately in the approval basis: a closest-point-of-approach or time-to-CPA criterion for 17(a)(ii), and for 17(b) the prediction-accuracy requirement, error tolerances and escalation to the master. Different ANS implementations will set different thresholds; the approval basis should bound that variation.

**Rule 19 — restricted visibility.**

*Requirement.* Safe speed adapted to restricted visibility; a vessel detecting another by radar alone must determine whether a close-quarters situation is developing, and certain alterations of course are to be avoided.

*Friction.* The Rule assumes radar as the primary sensor; a MASS may fuse several sensors, so "detects by radar alone" does not map directly.

*Recommended approach.* Declare a restricted-visibility mode, its sensor assumptions, speed policy and prohibited manoeuvres, and define the fusion state treated as equivalent to "radar alone".

**Parts C and D — lights, shapes, sound and light signals.**

*Requirement.* Rules 20 to 37 prescribe lights, shapes and signals, including sound signals in restricted visibility (Rule 35).

*Code treatment.* COLREG applies; the Code has no dedicated chapter on lights, shapes or sound signals.

*Friction.* The gap is verification and implementation, not applicability. The Code does not say who or what activates sound signals with no crew, or how Parts C and D are checked in surveys of an unmanned ship.

*Recommended approach.* Provide a survey and verification checklist for lights, shapes and signals, including automated sound-signal activation on detection of restricted visibility, fault monitoring, and manual or remote override. A summary of a UK small-workboat code reports a requirement to show not-under-command signals on loss of connectivity; the text has not been reviewed here.

**Part F — verification of compliance.**

*Requirement.* Rules 39 to 41, adopted in 2013 and in force from 2016, subject each Contracting Party to periodic audit against the IMO Instruments Implementation Code.

*Friction.* COLREG verification operates at flag-State level; the Code verifies at vessel and ROC level.

*Recommended approach.* Treat the layers as distinct and cumulative (section 3.5).

### 3.3 SOLAS, ISM, ISPS and STCW

| Legacy requirement | MASS Code treatment | Nature of friction | Practical implication and recommended approach |
|---|---|---|---|
| SOLAS V/19, V/20 — navigational equipment; voyage data recorder | Specified requirements met "by electronic means" (ch. 16); V/20 applies to all MASS; logged data available to the Administration and investigators (9.10) | Written for a human navigator on a bridge; equipment must be remotely accessible and machine-readable | Declare how each V/19 requirement is met electronically and the back-up arrangement for charts. Resolved in principle; detail is per ship |
| SOLAS II-1 — structure, stability, watertight integrity | Stability computer continuously assesses intact stability and supports damage assessment (ch. 19); compliance with Load Lines and the IS Code (19.2.1) | Criteria assume crew corrective action (ballast, damage control) | Declare the monitoring and alerting function and the human or remote response chain; criteria still apply |
| SOLAS II-2 — fire | Remote and on-board control of active fire protection; interface for external fire responders (ch. 20) | Firefighting assumes crew | Automated detection, remote or autonomous extinction and an external-responder interface; validate single-compartment fire control and fallback logic |
| SOLAS III, V/33 — life-saving appliances; assistance to persons in distress | Rescue equipment usable independently of crew; accommodation for retrieved persons (ch. 21) | Chapter III assumes crew; the duty to assist persists | Declare crewless deployment, accommodation for rescued persons and their communication with the ROC |
| SOLAS XI-2, ISPS Code — ship security | Ship security plan accounts for the ROC; remote operators take part in security training and drills; ROC breach triggers fallback (ch. 12) | The ROC becomes a security target; no on-board security officer | Extend the plan to the ROC. Remote operators inherit specific transferred duties; they should not be assumed to replace the ship security officer automatically |
| SOLAS IX, ISM Code — safety management | ROC safety management system; alternative document of compliance and certificate arrangements (ch. 11) | The ISM chain (Company, master, crew) does not account for a ROC as a further node | Use the ship's SMS with a ROC SMS; define interfaces among Company, ship, ROC and master |
| STCW — training, certification, watchkeeping, sea service | Remote operators qualified to a level not less than STCW; ROC may be treated as a location directly associated with the bridge; remote operating experience may be considered equivalent to sea service; fatigue principles apply (ch. 14) | Remote operators are not on-board watchkeepers; rest-hour and workload implementation for ROCs is unquantified; IMO's scoping identified whether a remote operator is a seafarer as a high-priority question | Declare rest-hour records, workload limits, multi-ship alarm-load assessment and the basis for treating remote experience as equivalent |

### 3.4 MARPOL

The Code is supplementary to other instruments, so MARPOL applies to a MASS as to any ship. The Code contains no annex-by-annex mapping. IMO has tasked a sub-committee with scoping and gap analysis of MARPOL-side instruments; no output was found when this paper was prepared.

| Legacy requirement | MASS Code treatment | Nature of friction | Practical implication and recommended approach |
|---|---|---|---|
| Annex I — oil pollution; discharge monitoring; IOPP certification | No Annex I provision (data and machinery chapters only) | Machinery spaces may be unmanned; monitoring must be automated; survey treatment of unmanned spaces unclear | Annex I applies unchanged. Declare automated discharge monitoring and logging, and agree with the Administration how the IOPP survey treats unmanned machinery spaces |
| Annex IV — sewage | Modes with persons on board are recognized (ch. 2, 21) | "No crew" does not mean no persons: maintenance crews, pilots, rescued persons and mixed modes | Declare zero-person periods and holding or reception arrangements; apply Annex IV whenever persons are present |
| Annex V — garbage | Garbage not addressed specifically (ch. 22, 24) | Garbage arises from cargo residue, stores, maintenance, equipment and persons even without permanent crew | A garbage-management plan by voyage phase and person-presence mode |
| Annex VI — air pollution and efficiency | Machinery chapter addresses safe, reliable machinery, not emissions (ch. 24) | Alternative propulsion (electric, hybrid, wind assist) may raise fuel and equipment questions | Declare propulsion type and the compliance route, including any equivalence relied on |
| Protocol I — reports on incidents involving harmful substances | Logged data available to the Administration and investigators on request (9.10) | Data availability is not an immediate report; who reports (ANS, remote operator, master)? | Assign the reporting duty to master, Company or ROC in the ConOps and SMS; automate detection and logging |

### 3.5 Other instruments and cross-cutting issues

**Load Lines and the IS Code.** The Code requires compliance (19.2.1). Compliance mapping and verification against the operative texts should be included in stability and certification documentation.

**Amendment drift.** SOLAS and MARPOL amendments adopted in 2023–2026 enter into force on different dates, some after the Code is expected to become mandatory. An approval basis may be proved against a rule version that then changes. The approval basis should name the version of each instrument relied on and maintain a table of adopted, accepted, in-force and applicable amendments, with defined triggers for updating.

**The application gate.** The Code applies only when the Administration considers other instruments impracticable or insufficient. The Administration's decision on that point, the instruments found insufficient and the chapters invoked should be recorded in the MASS Record and approval basis.

**Layers of verification.** Four regimes overlap at different granularity and should not be collapsed into one: (1) flag-State implementation audit under the III Code, made mandatory through SOLAS chapter XIII; (2) COLREG Part F, audit of the Convention's implementation; (3) casualty investigation under SOLAS XI-1/6; and (4) vessel and ROC survey and approval under the Code. No strict hierarchy among them is asserted.

**Rule-set plurality.** International and national inland rules differ in places. A ship that crosses demarcation lines changes the rules that govern it; the ConOps should declare the rule set by geography and the V&V should test the transition.

**Cyber and non-cooperative targets.** A cyber event can degrade situational awareness or control and so cause navigational non-compliance (for example degraded look-out). This linkage is an inference, not stated in the instruments, but cyber risk assessment should be connected to COLREG-critical functions, with defined cyber-induced degraded states. Real encounters also include vessels that are non-compliant, deceptive or poorly detectable; scenario-based V&V and declared escalation limits are recommended.

### 3.6 Responsibility allocation

Navigation-safety responsibility is divided among instruments:

| Party | Principal source of responsibility |
|---|---|
| Flag State / Administration | SOLAS; approval and certification under the Code's approval process |
| Company | ISM Code; operation and management of the ROC |
| ROC | Code chapters on remote operation; ROC safety management |
| Master (aboard or remote) | COLREG Rule 2; Code (master responsible at all times) |
| ANS | Function performed under the master's authority; not a legal person |

The ISM triangle of Company, master and crew becomes, in practice, a quadrilateral of Company, ship, ROC and master. IMO's joint working group reportedly agreed, as GAO recorded in 2024, that an autonomous ship should have a human master, on board or remote, who can take control; that a ship may have more than one master over a voyage but only one ROC responsible at any one time; and that a master may in some circumstances be responsible for several ships. The last point raises workload and common-cause questions that the Code does not quantify.

**Recommended approach.** Maintain a responsibility-allocation matrix from flag State to ANS in the ConOps and task-allocation summary. The approval process should check that no responsibility is left without an owner, particularly at the handover between ANS and master and at the boundary between Company and ROC. Declare the limits of ANS authority.

Audited naval programmes illustrate the risk: in GAO's reports the Navy lacked an empowered leader for its whole uncrewed effort (2022), and leadership turnover and unformalized stakeholder roles still created inefficiency (2026). Those are military findings, used here only as analogy.

### 3.7 National law and regulator practice

**Statutory crewing (United States).** GAO reported in 2024, and repeated in testimony in December 2025, that statutes set minimum crew and credential requirements which the Coast Guard has no authority to waive for autonomous vessels outside a narrow pilot. The statutes read for this paper show the following scope:

- Title 46 U.S.C. § 8301 sets minimum numbers of licensed individuals for vessels subject to inspection, with exceptions (for example vessels operating only on rivers, harbours, bays and similar waters); the Secretary may suspend the chapter in a presidentially declared national emergency.
- § 8101 requires the certificate of inspection to state the complement of licensed individuals and crew considered necessary; the Secretary may modify it by endorsement. The complement above the statutory floor is therefore an administrative figure set per vessel.
- § 8102 requires watchmen on passenger vessels at night; § 8103(a) restricts certain officer positions on documented vessels to US citizens.
- § 8502 requires a federal pilot for coastwise seagoing vessels that are not sailing on register, within the territorial-sea baseline and inspected as specified; it is narrower than GAO's summary of a pilot "generally" being required.
- The at-sea recovery pilot enacted in 2022 allows the Secretary to waive navigation and manning laws for the pilot, excludes foreign vessels, and does not allow waiver of regulations arising under international conventions. The Coast Guard's description adds that each vessel is to be supervised at all times by a licensed human operator.
- A Coast Guard work instruction dated 1 June 2026 directs local officers not to set manning below the statutory minimum and says headquarters may consider reductions below its guideline manning, but not below the statute.

*Implication.* The Code's equivalence test (that an alternative achieves the safety level of a conventional ship) is an approval criterion; it does not amend a domestic statute. A MASS may be approvable under the Code and still require the statutory complement. Submitters should not assume labour savings that the flag State's statutes do not permit. Whether other flag States have comparable statutes is unsurveyed; flag States with such statutes may consider whether legislative flexibility is needed before a mandatory code takes effect.

**US Coast Guard practice.** The Coast Guard handles autonomous operations through local Captains of the Port and Officers in Charge, Marine Inspection, case by case. GAO reported (2024) that the process is resource intensive, that industry raised consistency concerns across ports, that the Coast Guard had issued no autonomous-specific regulation since 1987–88, and that it did not then intend to amend regulations or issue autonomous-ship policy guidance ahead of the IMO framework. A policy letter on human-supervised testing (22-01, Change 1) has since been cancelled by the June 2026 work instruction. That instruction is non-binding by its own terms and says the Code does not directly apply to the unmanned systems it covers, but it is informative: operators are asked for a ConOps covering control modes, remote-operator procedures and training, emergency procedures and cyber resilience, and for a COLREGS compliance statement explaining how look-out, manoeuvrability, navigation and lighting requirements will be met. Local officers forward test proposals for a national recommendation while retaining final approval authority.

Existing US regulations on automated vessels are a useful precedent for staged approval. Section 15.715 of 46 CFR bases acceptance of automation that replaces crew on the system's capabilities, its demonstrated and continuing reliability and a planned maintenance programme, and provides that until the system is proven reliable the certificate specifies manning adequate to operate in a continuously attended mode. It is an analogy for how evidence of reliability can relax manning, not a substitute for Code approval.

**Other countries (as reported in 2024; texts partly reviewed).**

- *Canada:* a Tier I policy (TP 13585, effective 1 February 2022) covers small autonomous surface ships of degree three or four, without crew or passengers, of 12 metres or less or 15 gross tons or less, and routes requests for alternative safety requirements to a technical review board. A separate Tier I policy on autonomous navigation systems aboard vessels exists and was not reviewed.
- *United Kingdom:* regulations in force since 13 December 2023 (SI 2023/1216) define remotely operated unmanned vessels under 24 metres and require the log book to be kept at the remote operation centre. For larger ships, GAO reported that autonomous operations are handled through exemptions and equivalences for each voyage, with the burden growing with size and autonomy.
- *Norway:* a 2020 circular on automation and unmanned operation applies existing law by ship type, uses the IMO equivalence process, and the owner of the Yara Birkeland has operated with a reduced crew of three after tests, with remote monitoring ashore.

**Liability (United States).** Under the rule in *The Pennsylvania*, 86 U.S. (19 Wall.) 125 (decided at the 1873 term), a vessel that breaks a statutory rule meant to prevent collisions bears a burden of showing the breach could not have been a cause. Later appellate formulations are softer (for example, clear and convincing proof that the breach could not reasonably be held a proximate cause). GAO observed that which autonomous technologies satisfy the look-out rule may therefore bear on civil liability, and that causation questions are unusual: a defective navigation system, improper engagement or disengagement of the system by an operator, or a system choosing between outcomes. Whether and how the rule applies to an autonomous vessel's look-out is a question for counsel. The practical point is that look-out equivalence evidence, verification records and retained data logs are the material on which such a dispute would turn.

### 3.8 Lessons from audited naval autonomy programmes (analogy only)

GAO's 2022 and 2026 reports on US Navy uncrewed and robotic autonomous systems are not regulatory sources. They are used here because they document, with audit evidence, institutional frictions that civil approval will also meet:

- **Common enablers were underfunded relative to vehicles.** Of about $1.9 billion spent on uncrewed maritime systems since 2015, only $293 million was requested for the digital infrastructure on which the vehicles depend; several early vehicles did not conform to the planned common autonomy architecture, risking retrofit (2022).
- **Crew checks must be re-created as software checks.** A key effort for uncrewed vessels was converting certifications once executed by the crew into certifications executed by software, which would take years; prototyping plans listed needed certifications without saying how prototypes would be used to develop them (2022). Civil MASS face the same conversion for crew checks that underpin SOLAS and COLREG compliance.
- **Readiness criteria and schedules were missing.** The Navy lacked measurable criteria for when a prototype was ready for acquisition and an integrated schedule linking evidence to decisions, with a risk of concurrency (2022).
- **Crew-reduction economics were unproven.** The Navy had not determined how many sailors uncrewed systems require ashore or aboard host ships, and earlier automation-driven crew reduction had raised maintenance cost and led to added crew when automated systems failed (2022).
- **Fixed early requirements conflicted with iterative development.** Commercial developers iterate and incorporate updates quickly; the Navy's linear approach produced long timelines and capabilities that lost relevance (2026).
- **Domain silos and leadership turnover impeded common capabilities,** and GAO recommended managing the effort as a portfolio with formalized stakeholder roles (2026).

*Implications for civil approval.* An approval basis should list the crew-performed checks now performed by the ANS or ROC and state when evidence for each will exist; state acceptance criteria and the timing of evidence relative to the approval decision; declare staffing and workload assumptions with fallback staffing for automation failure; and declare a change-control classification (section 5.4).

---

## 4. Case Law: *Evergreen Marine (UK) Ltd v Nautical Challenge Ltd* [2021] UKSC 6 (*Ever Smart*)

### 4.1 Why the case matters for autonomous ships

COLREG's text is unchanged, and IMO has decided not to amend it for MASS at this stage. Where the Rules are ambiguous, the interpretation that governs an encounter is the one a court or Administration accepts. *Ever Smart* is the most authoritative recent English-law analysis of how the narrow-channel and crossing rules interact, and its reasoning is unusually concrete about what a vessel can observe. That makes it a rare source of tests that can be coded and verified. It is UK law; it is persuasive, not binding, in other jurisdictions, and a submitter should say which interpretation it relies on.

**"In sight" and the sensor-fusion problem.** The crossing rules sit in Part B, Section II, headed conduct of vessels in sight of one another. "Sight" means visual sight, not visibility on radar or AIS (Rule 3(k); judgment para 46). The Court also said the Rules should not be construed on the assumption that every vessel carries radar or AIS, and that the basic way to identify risk of collision remains repeated observation of compass bearing (paras 72–73). For an ANS built on fused sensors, the approval basis should therefore declare (a) which fusion states count as "in sight" for Section II, (b) the rule set applied when a target is detected only by sensors, and (c) how bearing steadiness is measured.

### 4.2 Holdings relevant to ANS design

Paragraph references are those recorded in the source analysis for this paper, checked in part. Paragraphs 40, 61, 77–84, 98 and 108–112 have been checked against the judgment text. The narrow-channel conclusion (paras 134–145) is confirmed in substance, including against the Court's press summary, but paragraphs 119 onward of the full text were not read, so the group definitions and paragraph numbers for the three situations should be checked before citation (section 7.1).

1. **Crossing rules versus narrow-channel rules (paras 134–145).** Where an outbound vessel in a narrow channel is crossing with an approaching vessel so as to involve risk of collision, the crossing rules are not displaced merely because the approaching vessel intends or is preparing to enter the channel. They are displaced only if and when the approaching vessel is shaping to enter: adjusting her course to reach the entrance on her starboard side, on her final approach. The Court distinguished three situations: a vessel crossing the entrance without intending to enter (crossing rules apply); a vessel intending or preparing to enter but not yet shaping, for example waiting for a pilot (crossing rules still apply, and this was the position of the Alexandra 1); and a vessel shaping to enter on final approach (narrow-channel rules prevail).

2. **Steady bearing, not steady course (paras 111–112; see also 77–84, 108–112).** The engagement of the crossing rules does not depend on either vessel being on a steady course. The trigger is risk of collision, which Rule 7(d)(i) deems to exist if the compass bearing of an approaching vessel does not appreciably change. An erratic, slow, manoeuvring or waiting vessel is still subject to the crossing rules while the bearing is steady, subject to the conditions in item 5.

3. **Two circumstances under Rule 17 (para 61; para 60 concerns Rule 16).** Rule 17(a)(ii) is permissive: the stand-on vessel may act once it becomes apparent that the give-way vessel is not taking appropriate action. Rule 17(b) is mandatory: the stand-on vessel must act when collision cannot be avoided by the give-way vessel alone. The labels "observational" and "predictive" are this paper's; the Court's wording is that the obligation ends when it appears the give-way vessel is not complying, or when action by both vessels has become necessary.

4. **Timing and legibility of avoiding action (para 40, quoting The Maloja II).** Manoeuvres to avoid a close-quarters situation should be made at a time when the officer is not forced into a quick decision or one based on inadequate information, and should be readily apparent to the other ship.

5. **Observability (para 98(vii)).** Where taking bearings over time is not possible, particularly in crowded waters where the vessels' view of each other is impaired, curves or irregularities in one vessel's course may make it impossible for the other to ascertain a crossing situation, and the crossing rules are then not engaged. Engagement depends on how each vessel's conduct is reasonably observable by the other.

### 4.3 Design and verification implications

- **Do not require a steady course as a precondition.** An ANS that checks "is the other vessel on a steady course?" before applying the crossing rules will not meet the standard the Court set. Bearing rate of change, measured over time with adequate accuracy, is the minimum observable. A vessel that is waiting is not exempt from the crossing rules while its bearing is steady, provided she is moving across the ground to some extent (para 98(vi)).
- **Rule switching at channel entrances needs an explicit logic.** The distinction between preparing and shaping is the crux. A design needs observable criteria for shaping to enter and a defensible method for switching between rule sets (section 4.4).
- **Treat the two Rule 17 triggers as different algorithms** with different accuracy requirements, and verify them separately.
- **Make decision timing a declared parameter.** If the ANS decides late, any manoeuvre will fail the legibility test. The ConOps should state the maximum decision latency and the range at which avoiding action begins.
- **Declare the governing interpretation.** If the ship operates in the United Kingdom or a jurisdiction that follows the UK approach, encode it; otherwise state what is relied on.

### 4.4 Illustrative design logic for rule switching

The following is an illustration of how the first holding might be implemented. It is not a standard and has not been validated by any Administration, classification society or IMO body; the numeric parameters in Appendix A are placeholders to be set by vessel-specific verification.

**States.** (1) *Crossing:* the approaching vessel is not intending to enter, or intends to enter but is not yet shaping; crossing rules apply. (2) *Transition:* the approaching vessel is adjusting course toward the entrance but has not committed to final approach; crossing rules still apply, with enhanced monitoring and an advisory to the master. This state is an engineering buffer, not a category in the judgment. (3) *Shaping:* the approaching vessel is adjusting her course to reach the entrance on her starboard side, on final approach; narrow-channel rules prevail and the master or ROC is alerted that the rule set has changed.

**Observables.** Three conditions drive the transitions: (a) a sustained course adjustment; (b) whether the adjustment is directed at the entrance on her starboard side, using the entrance geometry from electronic charts, either by projected course alignment or by a projected lateral miss of the entrance within tolerance (Appendix A); (c) whether the vessel is on final approach (closing, not holding or station-keeping), using speed, distance to the entrance and, where available, pilot-boarding information.

**Known design questions.** A vessel already aligned with the entrance and closing but showing no detectable course adjustment would not trigger any transition as drawn, and whether such a vessel is "shaping to enter" is a design and approval question. There is no direct path from crossing to shaping, so a vessel that becomes aligned and closing within one update cycle must pass through the transition state. Reversion hysteresis should be defined to avoid oscillation at boundaries.

**Verification scenarios.** At least: a vessel crossing the entrance without intent to enter (the ANS stays in the crossing state throughout); a vessel shaping to enter on final approach (the switch occurs at the correct point); a vessel waiting for a pilot (crossing rules continue; no premature switch); a give-way vessel on an erratic course with steady bearing (crossing rules engage); and sensor degradation affecting bearing or closure-rate estimation (declared degraded behaviour and alert to the master).

**Degraded-state behaviour.** In the degraded state the ANS holds the last valid rule set, alerts the master, and treats risk of collision as deemed to exist (Rule 7(a)). Rule 17 actions are still available on that basis. In simulation, withholding them in the degraded state led to a collision in the sensor-degradation scenario.

**What the simulation shows.** An accompanying browser simulation implements the logic above and runs the five verification scenarios against simulated sensor noise. On the fixed random seeds all five produced the expected rule-set behaviour; with other seeds one run of the second scenario in 40 missed the switch (section 7.1). This demonstrates that the logic is coherent and testable. It does not validate it against real traffic, real sensor data, or any Administration's requirements.

### 4.5 Limits of the analysis

The holdings are of one national court and concern a particular collision. The illustration above translates legal tests into observables; the translation is an engineering interpretation and is not endorsed by the Court. No Administration or classification society has been identified as having adopted an equivalent rule-switching trigger, but practice outside the sources reviewed has not been surveyed.

---

## 5. Operational and Design Implications: Using the ConOps and Approval Basis

### 5.1 The interpretation layer the Code already contemplates

The Code's approval process centres on an approval basis submitted by the applicant and approved by the Administration. The ConOps is expected to identify possible deviations from applicable rules and regulations and to justify alternative solutions on the basis of risk assessment, and the MASS Record is to contain a regulatory gap analysis. Together these documents are the place where each friction in section 3 is resolved for a specific ship, without amending the underlying instrument.

This layer is not an IMO interpretation, which needs committee action; it is not a general flag-State circular; it is not an exemption or equivalent arrangement under the SOLAS equivalence provisions, which are separate mechanisms; and it is not a court ruling, although it may encode one. Its force comes from the Administration's approval and from national implementation, not from the non-mandatory Code. It is subject to re-assessment on change.

A distinction matters. Where an entry interprets the text (for example how "shaping to enter" is observed), it stays within the Rule. Where an entry would depart from the text, the departure must be justified through the ConOps, remains subject to the mandatory legacy provision, and depends on the flag State's own authority to accept it.

### 5.2 What the ConOps and approval basis should state

| Topic | The ConOps / approval basis should declare |
|---|---|
| Look-out (Rule 5) | Sensor suite; degradation modes; functional mapping to the Rule's elements; equivalence argument and test results, including small, low-signature targets |
| Remote master and latency (Rule 2) | Maximum detection-to-intervention interval; ANS fallback behaviour; authority transfer; limits of the vessel, ANS and link as Rule 2(b) limitations |
| Safe speed, scanty information (Rules 6, 7) | OE parameters derived from Rule 6 factors with margins and degraded-state buffers; sensor-sufficiency threshold and uncertainty floor |
| Legibility and timing (Rule 8) | Manoeuvre magnitude and timing criteria; legibility to human observers and to other MASS; maximum decision latency |
| Stand-on action (Rule 17) | Separate observation threshold for 17(a)(ii) and prediction requirements and escalation for 17(b) |
| Crossing engagement | That crossing rules engage on steady bearing, not steady course; bearing measurement accuracy; erratic-course scenarios |
| "In sight" and fusion | Which fusion states count as "in sight" for Section II; rule set applied when a target is detected only by sensors; how bearing steadiness is measured |
| Rule switching at channel entrances | Governing interpretation; observable criteria and transitions; verification scenarios |
| Restricted visibility (Rule 19) | Mode definition; sensor assumptions; speed policy; prohibited manoeuvres |
| Lights, shapes, signals | Automated sound-signal activation, fault monitoring, override; survey method for Parts C and D |
| Small MASS and rule sets | Rules applied; national measures relied on; behaviour in separation schemes; rule set by geography |
| Statutory complement | The flag State's required complement for each mode; how statutory roles (master, others) are met; the legal route relied on (statutory change, pilot authority, exemption, or none) |
| Responsibility | Matrix from flag State to ANS; verification that no responsibility is unowned; ANS authority limits |
| ROC watchkeeping | Rest-hour records; workload limits; multi-ship alarm-load assessment; basis for equivalence of remote experience |
| Security and safety management | ROC within the ship security plan; interfaces among Company, ship, ROC and master |
| MARPOL | Annex-by-annex compliance declaration, including unmanned machinery spaces, person-presence modes and reporting duty |
| Verification layers | Evidence for each of the four layers in section 3.5, kept distinct |
| Application gate and version | The Administration's application-gate decision; version of each instrument relied on; amendment horizon |
| Evidence retention | Retention and access arrangements for look-out evidence, verification results and data logs |

### 5.3 Acceptance criteria and timing of evidence

Each declared threshold should carry an acceptance criterion and a statement of when the supporting evidence will exist relative to the approval decision. The naval audit evidence in section 3.8 shows the cost of prototypes proceeding without measurable readiness criteria or an integrated schedule.

### 5.4 Change control

A version-locked approval basis meets software updated on a commercial cadence. The approval basis should classify changes: those that require re-assessment (for example changes to the ConOps, OE or software that alter declared behaviour); those pre-approved within declared bounds (for example parameter adjustments inside stated limits, with the supporting evidence); and those that are administrative. Whether an Administration will accept bounded pre-approval is not known; no flag-State practice on this was found.

### 5.5 Considerations by audience

- **Administrations.** The approval basis is the opportunity to check that each friction has a ship-specific resolution; a common risk-assessment framework for approvers reduces inconsistency, which US industry raised with the Coast Guard. Statutory complement and the legal route relied on should be stated at the outset.
- **Recognized organizations and surveyors.** Surveys should verify that declared thresholds are met and that Parts C and D arrangements work as declared, including failure modes.
- **Operators and ROC providers.** The declared thresholds are operationally significant; the safety management system should incorporate them and remote operators should be trained on them. Staffing assumptions should be validated against workload, with fallback staffing when automation fails.
- **Designers and autonomy developers.** Design for bearing-based engagement, separate Rule 17 logic, declared decision latency and explicit degraded states, and plan the evidence needed to show equivalence.

---

## 6. Transition Considerations, 2026–2032

**Legal position.** Until a mandatory code is in force, the binding baseline is the existing conventions and national law (section 2.3). The Code's value in this period is as a structured way to present an approval case.

**Timeline.** IMO's roadmap targets adoption of the mandatory code by 1 July 2030 and entry into force on 1 January 2032, with work on the mandatory code expected to begin in 2028. One report of MSC 111 says the Committee considered that 2032 might be unrealistic and that 2036 could be more appropriate, but agreed to keep the existing date, which can be revised later. The 2030, 2028 and 2036 points rest on secondary reports and have not been checked against the MSC 111 report (section 7.1).

**Practical stability of COLREG.** COLREG was last amended in 2013. IMO's 2021 scoping exercise had classed COLREG as a high-priority instrument and, for the highest degree of autonomy, pointed toward amendment as the most appropriate route. In 2023 the Maritime Safety Committee noted that COLREG requirements remain relevant and applicable regardless of how a ship is operated, and that there was no need to amend COLREG to accommodate MASS at this stage. An amendment under the Convention's procedure remains possible but is slow, and no cycle was identified in the sources reviewed. For planning purposes the Rules will not change before about 2032; this is a practical expectation, not a legal rule.

**Consequences.**

- Harmonization of the Rules with autonomous operation will occur through interpretation in individual approvals, not amendment.
- The first Administrations to approve MASS with well-reasoned interpretations may set de facto practice. That is a prediction, not a finding.
- IMO officials were reported in 2024 as saying that the non-mandatory framework needs to be right the first time because later changes would be difficult; the same reasoning applies to early approval precedents.

**National implementation.** Flag States may make the Code mandatory nationally, and contracts or class requirements may impose it earlier. Where they do not, the Code is applied unevenly while legacy duties remain binding. Certificates and approvals should say what was applied.

**Statutes and pilots.** Where domestic statutes fix complement or credentials, relief currently comes from narrow pilot authorities (in the United States, the 2022 at-sea recovery pilot) or from statutory change. The Coast Guard has stated that it monitors developments and briefs Congress. Flag States with comparable statutes may wish to assess whether legislative flexibility is needed before 2032.

**Regulator practice.** Expect case-by-case review. The Coast Guard's approach in 2024 was to wait for the IMO framework and for the technology to reach critical mass before regulating; its 2026 work instruction reflects a more structured project-level process but is non-binding. Canada, the United Kingdom and Norway have small-vessel measures and exemptions. Operators should plan for resource-intensive review and for inconsistency between ports or offices.

The MARPOL, small-MASS and ROC-workload items have no IMO-level resolution in this period; they will be handled by national practice and by the approval basis. IMO has started scoping work on MARPOL-side instruments and has a legal road map; neither had produced output when this paper was prepared.

**Evidence accumulation.** The experience-building phase planned after adoption will be only as useful as the evidence it gathers. Submitters who record and share anonymized reference test protocols for look-out equivalence, handover latency and rule-switching verification would help reduce the situation in which each applicant argues from scratch.

---

## 7. Open Issues and Verification Needs

### 7.1 Verification status

This table states what was checked, against what, and what remains. "Primary or official text" means the instrument, statute, regulation, judgment or official document itself; "secondary" means a summary, aggregator or commentary.

| Item | Status | Basis and remaining work |
|---|---|---|
| Adoption date, effect date and non-mandatory status of MSC.595(111) | Verified against official text | Resolution text on the IMO website records adoption on 21 May 2026 (MSC 111 sat 13–22 May 2026; some summaries give 22 May, the session's closing day); effect and status from meeting summaries. The resolution cover and footnote also record a re-issue on 10 September 2026 to add the date (cover excerpts only read) [P] |
| Roadmap and 1 January 2032 target | Verified as a target only | IMO-side summaries; "earliest" and "may be revisited"; the annexed roadmap itself was not re-read |
| Roadmap details (2030 adoption target; work from 2028; 2036 remark) | Not verified | Secondary and trade-press reports only; check against the MSC 111 report and the annexed roadmap |
| COLREG Rules 1–30 and Part F | Verified against primary or official text | US Coast Guard amalgamated text and IMO resolution A.1085(28); Rules 31–41 confirmed at heading level; text of Rules 32–37 beyond headings not read |
| MSC 107 decision on COLREG amendment | Confirmed in secondary summaries | DNV and a class technical circular. Report number is MSC 107/20. Paragraphs 5.48–5.49 not confirmed. Check the report text |
| IMO scoping outcome (MSC.1/Circ.1638) | Partly verified | Annex pages 1–66 read, including the degree and priority tables; the COLREG appendix was not read |
| *Ever Smart* holdings and paragraph numbers | Partly verified | Verified against the judgment text for paras 1–118 and against the Court's press summary for the narrow-channel conclusion. Paras 119 onward to be read before citation |
| MASS Code paragraph references | Not re-verified for this paper | Carried from earlier reading of the adopted text; check against the official publication |
| SOLAS, STCW, Load Lines, IS Code, MARPOL operative text | Not verified against consolidated texts | Treatment is at the level of principle; check operative provisions before relying on any detail |
| US statutes (46 U.S.C. §§ 8101, 8102, 8103, 8301, 8502, 4312) and the 2022 pilot | Verified against statutory text | Currency checked to late 2026 for most sections; § 8301 as of December 2025; definition of "master" (§ 10101) only through GAO; pilot start and end dates not confirmed |
| US Coast Guard work instruction of 1 June 2026 | Verified against the document | Read in full; non-binding |
| Coast Guard policy letter 01-23 | Verified | Policy letter cited by GAO as 01-20 |
| Marine Safety Manual Vol. III | Not verified | Not located / not read; not relied on |
| 46 C.F.R. § 15.715 and § 62.50 | Verified in part | § 15.715 and § 62.50-1 read; § 62.50-30 confirmed to exist |
| Canada, UK, Norway measures | Confirmed in excerpts | Annexes and companion texts not read; a signalling requirement GAO attributed to the Canadian policy was not seen in the excerpts |
| GAO reports of 2022, 2024, 2026 | Read in full | The December 2025 testimony was seen only in excerpts |
| The Pennsylvania rule | Verified as doctrine | Application to autonomous vessels not examined; one cited appellate case not checked |
| FY2026 NDAA provisions on naval acquisition | Verified in part | The specific repeal provision rests on GAO's report |
| Treaty status and amendment-in-force data | Not verified in this paper | Check against IMO's status database |
| Browser simulation (rule_switching_demo.html) | Partly verified | Logic run headless on 15 November 2026 against the five scenarios: all pass on the fixed seeds. In a 40-seed check, scenarios 1, 3, 4 and 5 passed every seed and scenario 2 passed 39 (one run never left the crossing state, a missed detection under noise). Withholding Rule 17 action in the degraded state causes a collision in scenario 5. Not run in a browser; not validated against real traffic or sensor data. Station-keeping is an instantaneous speed gate only |
| Independent technical review | Not done | |

### 7.2 Open substantive questions

1. **Reference evidence for look-out equivalence.** No accepted test or benchmark was identified. Whether flag States, classification societies or IMO will publish one is unknown.
2. **Thresholds.** Handover latency, sensor sufficiency and prediction accuracy are unspecified by the Code and by any source reviewed.
3. **MARPOL.** An annex-by-annex mapping, and survey treatment of unmanned machinery spaces, remain to be done.
4. **Small MASS.** No IMO-level regime; national practice varies and has been surveyed only for four jurisdictions.
5. **ROC workload.** Quantification of rest and alarm load, especially where one master or ROC covers several ships.
6. **Statutory flexibility.** Whether and when legislatures will address minimum-complement statutes.
7. **Liability.** Application of presumptions such as the Pennsylvania rule to autonomous vessels; effect of IMO's legal work.
8. **Civil–military interaction.** Warships and government ships are outside the Code, and no source reviewed addresses encounter conduct between them and civil MASS.
9. **Change control.** Whether Administrations will accept bounded pre-approval of software changes.
10. **Other jurisdictions and the *Ever Smart* test.** Whether other courts or Administrations adopt it, and whether any adopt a different observable trigger.

---

## 8. Glossary

- **ANS** — autonomous navigation system.
- **Approval basis** — the vessel-specific document, submitted by the applicant and approved by the Administration, on which approval and certification rest.
- **ConOps** — concept of operations.
- **COTP / OCMI** — US Coast Guard Captain of the Port; Officer in Charge, Marine Inspection.
- **Degrees of autonomy** — IMO scoping categories one to four (section 2.4).
- **MASS** — maritime autonomous surface ship.
- **MASS Record** — document under the Code containing, among other things, the regulatory gap analysis.
- **OE** — operational envelope.
- **ROC** — remote operations centre.
- **Regulatory gap analysis** — the analysis of how a ship meets, or justifiably departs from, applicable rules.

## 9. Sources

**IMO and treaty instruments.** Resolution MSC.595(111), International Code of Safety for Maritime Autonomous Surface Ships (adopted 21 May 2026). MSC.1/Circ.1638, Outcome of the Regulatory Scoping Exercise for the Use of Maritime Autonomous Surface Ships (3 June 2021). Report of the Maritime Safety Committee on its 107th session (May 2023), MSC 107/20 (paragraph references 5.48–5.49 not confirmed). IMO Assembly resolution A.1085(28), amendments to COLREG (Part F). Convention on the International Regulations for Preventing Collisions at Sea, 1972, as amended (US Coast Guard Navigation Center amalgamated text). SOLAS, MARPOL, STCW, the ISM and ISPS Codes (not re-verified here).

**Case law.** *Evergreen Marine (UK) Ltd v Nautical Challenge Ltd* [2021] UKSC 6. *The Pennsylvania*, 86 U.S. (19 Wall.) 125 (1873 term). *The Maloja II* (as quoted in the *Ever Smart* judgment).

**US Government.** GAO-22-104567, *Uncrewed Maritime Systems: Navy Should Improve Its Approach to Maximize Early Investments* (April 2022). GAO-24-107059, *Coast Guard: Autonomous Ships and Efforts to Regulate Them* (8 August 2024). GAO-26-109014, *Robotic Autonomous Systems: Navy Needs to Address Leadership and Organizational Challenges to Meet Urgent Needs* (15 June 2026). GAO-26-108762, *Coast Guard: Approaches to Autonomous Ship Regulation* (testimony, December 2025; excerpts only). US Coast Guard Work Instruction 5P-WI-002(1), *Oversight of Unmanned, Autonomous and Remote-Control Operations* (1 June 2026). US Coast Guard CG-ENG Policy Letter 01-23, *Design Basis Agreement Submission Guidance* (17 March 2023). 46 U.S.C. §§ 8101, 8102, 8103, 8301, 8502, 4312; 14 U.S.C. § 501 note (at-sea recovery pilot, FY2023 NDAA § 11504); 46 C.F.R. §§ 15.715, 62.50. 33 C.F.R. Part 83. FY2026 National Defense Authorization Act (Pub. L. 119-60).

**Other national measures.** Transport Canada, Tier I Policy TP 13585, *Oversight of Small Maritime Autonomous Surface Ships* (effective 1 February 2022). UK Merchant Shipping (Small Workboats and Pilot Boats) Regulations 2023, SI 2023/1216. Norwegian Maritime Authority, circular RSV 12-2020 (27 August 2020) and presentations to IMO.

---

## Appendix A. Illustrative Parameters for the Rule-Switching Logic in Section 4.4

These values are engineering placeholders offered to make the logic concrete. They are not derived from the *Ever Smart* judgment, which supplies the legal test but no numbers. They have not been validated and should be set, justified and verified for each vessel and operating area. The values marked "simulation" are those used in the accompanying browser simulation; none is derived from the judgment or validated.

| Parameter | Placeholder | Purpose |
|---|---|---|
| Course-adjustment detection | Sustained course change of at least 5° over at least 60 seconds | Separate genuine manoeuvres from noise |
| Course filter | Low-pass over about 60 seconds before applying the course-adjustment test (simulation) | Prevent rapid heading oscillation with steady bearing from triggering a transition |
| Alignment with entrance | Projected course within about 10° of the bearing to the entrance's starboard side, or a projected lateral miss of that point within the lateral tolerance | Identify a vessel reaching the entrance on her starboard side |
| Lateral miss of entrance | About 0.12 nm (half the channel width) (simulation) | Accept a vessel whose projected track passes within the entrance, even where the bearing angle is large at short range |
| Final approach | Distance to entrance decreasing at about 0.5 knots or more and within about 2 nautical miles | Distinguish final approach from holding |
| Station-keeping | Speed over ground of about 1 knot or less for about 5 minutes, or heading oscillation without net closure (simulation: an instantaneous speed gate only; the 5-minute duration and the oscillation test are not implemented) | Identify a vessel waiting (for example for a pilot) |
| Dwell before forward transition | About 30 seconds of the conditions holding continuously (simulation) | Avoid premature forward transitions |
| Reversion hysteresis | State persists about 30 seconds before reverting | Avoid oscillation at boundaries |
| Steady-bearing limit | About 0.05°/s (simulation) | Detect a steady bearing |
| Rule 17(a)(ii) action permitted | TCPA below about 480 s and CPA below about 0.5 nm (simulation) | Permit own action when the give-way vessel is not acting |
| Rule 17(b) action required | TCPA below about 180 s and CPA below about 0.2 nm (simulation) | Require own action when collision cannot be avoided by the give-way vessel alone |
| Degraded-state trigger | Bearing-fit residual above about 1.5° for about 20 seconds, or loss of radar (simulation) | Declare degraded state and alert the master |
| Degraded-state recovery | About 30 seconds below the degradation threshold (simulation) | Resume normal state logic |

**Sensor performance.** The logic needs bearing, range and course information from radar and AIS, entrance geometry from electronic charts conforming to the IHO ENC product specification (with chart data-quality values reviewed), visual confirmation of aspect and lights, and own-ship position. No sensor accuracy figures are proposed here because no source reviewed supports specific values; they should be set from vessel-specific verification. If radar is unavailable, AIS with electro-optical sensing may support the course and geometry conditions but not the closure-rate condition; if both radar and AIS are unavailable the ANS should enter a declared degraded state and alert the master.
