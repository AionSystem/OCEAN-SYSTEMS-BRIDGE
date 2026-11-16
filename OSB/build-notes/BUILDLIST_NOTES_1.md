BUILD LIST: OSB Mother-Node Expansion & DSM-UCFS Integration
Field
Value
Document
OSB-BL v0.1 — Build list for next file cycle
Role
Requirements brief. Input to the AI updating UCFS / ARCVB / IAAP. Not a specification, not a standard, not legal advice.
Applies to
Next builds of UCFS, ARCVB, IAAP + new OSB layer + new DSM-UCFS domain pack
Status
Working brief. Every item is [P] until traced against the current file set.
Sequencing
Apply AFTER the three incoming updated files are merged. Re-trace before writing. See §9.
Conventions
MUST / MUST NOT / SHOULD / SHOULD NOT / MAY in the RFC 2119 sense. [P] as defined in UCFS v0.3 §2.2.
1 — The one architectural decision this build rests on
OSB-BL-001 [DECISION, owner: author]. The stack generalizes from "MASS stack" to "OSB ecosystem" by separating a stable core from domain packs:
Core (domain-neutral): the claim model (status × compression-type mapping, UCFS §8.3.10), gates G0–G6, evidence tiers E1–E4, [P] discipline, non-waivable mechanism, version lock, ledger, runtime monitors. These MUST NOT change per domain.
Domain packs: each ocean problem domain is a pack that plugs into the core. MASS-UCFS is the first (existing). DSM-UCFS (deep-sea mining / ISA) is the second pack to build in this cycle. BIO-UCFS (sargassum / pelagic ecology) is third, stubbed only.
OSB-BL-002. UCFS's core clauses (claim attributes §8.2.1, status §8.1, compression types §8.3, gates §5, evidence tiers §8.5, [P] §2.2, NW mechanism §5.4) MUST remain applicable to both MASS and DSM without modification. If a build item requires changing a core clause to fit DSM, that item MUST be recorded as an open item, not silently changed.
OSB-BL-003. The domain taxonomy (UCFS §6.3, currently D-A…D-N) MUST be made extensible. MASS domains remain D-A…D-N. DSM domains are a new series (proposed D-O.*). Do not renumber D-A…D-N — ARCVB Annex B and IAAP §6.1 hard-reference them.
2 — New layer: OSB Mother Node
OSB-BL-010. Create a short OSB layer document (new file, not inside UCFS). It is a framing/governance layer, not normative. It MUST state:
OSB (Ocean Systems Bridge) is the ecosystem / mother node; UCFS is the consensus protocol; ARCVB is the execution pipeline; IAAP is the adoption layer.
The relationship diagram (Layer 4 IAAP → Layer 3 UCFS → Layer 2 ARCVB → Layer 1 source/friction map), now generalized: "Layer 1" is per-domain (MASS Regulatory Bridge for MASS; DSM Friction & Baseline Map for deep-sea mining).
OSB is adopter-agnostic and domain-extensible.
A naming-discipline note: public institutional name is Ocean Systems Bridge (OSB). [P] whether any counterparty has been engaged under this name.
OSB-BL-011. OSB-BL-010 MUST NOT claim any institutional role, endorsement, or authority. Mirror the notice-block discipline from IAAP and UCFS verbatim in spirit.
3 — UCFS next-build items (DSM-UCFS domain pack)
3.1 New domain taxonomy (DSM)
OSB-BL-020. Add a DSM domain series [P] (benthic/pelagic science is unsettled; every item is provisional until baselined):
Ref
Domain
Scope
Source (2025 notes)
D-O.1
Benthic baseline & habitat
Nodule distribution (uneven), megafauna abundance, low density/high diversity, 26-yr track persistence
notes §1
D-O.2
Electrochemical function ("dark oxygen")
Nodules as oxygen generators; chamber oxygen decline; removal = chemical alteration, not just physical
notes §1 (Sweetman)
D-O.3
Sediment & plume dynamics
Sediment concentration for abyssal fauna; benthic plumes; dewatering discharge ~50 m³/day
notes §1, §mid-water
D-O.4
Mid-water / pelagic discharge
Discharge depth (200 m vs 1500 m); OMZ interaction; mesoscale + seasonal/spatial variability; micronekton & zooplankton
notes §mid-water
D-O.5
Endemism & community structure
30–54% fish endemism at discharge depth; low-biomass diverse communities at 1500 m; high regional endemism
notes §mid-water
D-O.6
Toxicity & contamination
Cu toxicity rise with plume ascent; rotifer mortality vs controls; mercury bioaccumulation into deep dwellers → food chain
notes §mid-water
D-O.7
Food-web disruption
Particle feeders unable to feed in plume; mesopelagic food-supply reduction; contamination of food supply
notes §mid-water
D-O.8
Acoustic impact
Noise impact on marine mammals
notes §mid-water
D-O.9
Recovery timescales & temporal asymmetry
Nodules take millennia to form; abyssal plain full recovery ~100 yr; CCZ ecosystems "least resilient on Earth"
notes §1
D-O.10
Institutional / mandate
ISA mandate gap; no mining zones established ("national park without being in the country")
notes §ISA
OSB-BL-021. Each D-O.* domain MUST be assigned to a severity default and evidence-tier minimum in a DSM version of the §8.5.5 table. Proposed: D-O.2 (dark oxygen), D-O.6 (toxicity), D-O.9 (recovery) are S1-blocking until baselined [P].
3.2 DSM non-waivable list
OSB-BL-030. Define a DSM non-waivable list (parallel to MASS NW-1…NW-8), proposed [P]:
Ref
Non-waivable
Rationale
NW-O1
Benthic baseline & dark-oxygen function
Cannot claim mitigation without a baseline; D-O.2 is a chemical-function claim
NW-O2
Mid-water discharge toxicity
Cu/toxicity breach into OMZ or endemic layer is a hard stop
NW-O3
Plume containment integrity
Uncontained dewatering/benthic plume = operation not permitted
NW-O4
Acoustic telemetry
Continuous noise monitoring with escalation
NW-O5
Recovery-timescale honesty
Commercial ROI timeline MUST NOT be conflated with geological/ecological recovery timeline
OSB-BL-031. NW-O* follow the same rule as UCFS §5.4.2: residue in a non-waivable domain = S1; bounded claim in a non-waivable domain = S2 with mandatory runtime escalation.
3.3 DSM claim-model application
OSB-BL-040. State explicitly that DSM claims use the same five statuses and eight compression types as MASS. No new statuses. A DSM claim such as "plume filtration reduces benthic impact" is a bounded fallback claim (status bounded, compression bounded fallback) until E4 operational evidence exists.
OSB-BL-041. Flag the 2025 "engineering fix" ideas as [P] bounded claims, not closed claims. Specifically: "machine that collects plume and spits out water only" and "bring plume back to sea floor" MUST be recorded as open residues or bounded fallbacks with E2+E4 obligation, never as closed. They have no derivation protocol.
OSB-BL-042. Apply the re-open trigger mechanism (UCFS §3.34, §18.3) to DSM: publication of new baseline science (e.g., dark-oxygen findings) is a re-open trigger that voids prior approval bases. Record this as a Subsystem-D-equivalent drift rule for DSM.
4 — ARCVB next-build items
OSB-BL-050. Add an Oracle ingestion service to ARCVB cross-cutting services [P]. External authoritative data sources (NOAA metocean/hydrographic, ISA environmental baseline, acoustic monitors, plume turbidity sensors) are Oracles. Requirements:
ARCVB-OR-01: every Oracle input MUST carry a provenance record, a quality/confidence indicator, and a declared degradation behaviour (mirrors ARCVB-IF-01, IF-02).
ARCVB-OR-02: Oracle loss or schema change MUST lower the sufficiency state of dependent claims, not be silently ignored.
ARCVB-OR-03: Oracle degradation MUST trigger the same escalation path as sensor degradation (Subsystem B pattern).
OSB-BL-051. Define the Oracle Problem as a named open item: how the stack treats a wrong, stale, or spoofed external feed. Map to existing PNT-denial / AIS-spoofing handling (UCFS §20.2, §20.3) as the precedent.
OSB-BL-052. For DSM, the runtime monitor (ARCVB §6.2) binds to environmental telemetry: turbidity, Cu concentration, acoustic levels, discharge depth. A threshold breach MUST raise an escalation event and (for NW-O domains) halt or bound the operation. Mirror ARCVB-RM-01…RM-07.
OSB-BL-053. Reuse the tamper-evident ledger (ARCVB §6.5) unchanged for DSM: environmental telemetry, escalation events, and halt events are ledger records. Do NOT create a separate DSM ledger. One ledger, multiple domains.
5 — IAAP next-build items
OSB-BL-060. Add a new counterparty class to the IAAP §2 matrix [P]: International Seabed Authority / ISA, and environmental science bodies / coastal states. Proposed cells:
Field
ISA [P]
Primary institutional fear
Approving extraction under an unsettled baseline; mandate gap; precautionary-principle conflict with commercial pressure
What they need
A continuous, auditable environmental-telemetry ledger; bounded claims with hard stops; baseline honesty
Architectural wedge
NW-O list + bounded-claim runtime escalation + ledger integrity
Wedge limit
Not an approval; ISA still decides. NW-O3 plume containment cannot be waived by UCFS or ISA
OSB-BL-061. Add a second counterparty cell [P]: mining & resource companies (adopters/counterparties), whose primary fear is stranded capital and permitting delay; wedge = bounded pre-approval + version-locked approval basis (mirror IAAP §2.2.5 commercial-developer wedge).
OSB-BL-062. Add a NOAA / data-authority note to IAAP: NOAA and equivalent bodies are Oracles, not counterparties. IAAP governs engagement with institutions that decide; Oracles are data sources feeding ARCVB. Do not conflate.
OSB-BL-063. IAAP Phase 1 (Zero-Threat Diagnostic) example for DSM: "Your current EIS relies on a pre-dark-oxygen baseline and does not state how mid-water discharge Cu toxicity is monitored in real time against the OMZ." This is the DSM equivalent of the MASS Rule 17(b) diagnostic sentence.
6 — Map the 2025 DSM notes into the friction register
OSB-BL-070. Build a DSM Friction & Baseline Map (the DSM Layer-1 document, parallel to the MASS Regulatory Bridge). Seed it from the 2025 notes. Every item [P] until verified against primary science/policy text:
#
Friction / uncertainty
Domain
Status in brief
O1
Nodules unevenly distributed; low density / high diversity
D-O.1
[P]
O2
Dark oxygen: nodules produce oxygen; chamber decline
D-O.2
[P] — verify Sweetman primary text
O3
26-yr-old tracks still present; ~100 yr full recovery; millennia to form nodules
D-O.9
[P]
O4
Sediment concentration impacts abyssal fauna
D-O.3
[P]
O5
Dewatering ~50 m³/day; chemical + sediment plumes
D-O.3, D-O.4
[P]
O6
Discharge depth question (200 m vs 1500 m); OMZ interaction
D-O.4
[P]
O7
30–54% fish endemism at discharge depth
D-O.5
[P]
O8
Cu toxicity rises with plume ascent; rotifer mortality vs controls
D-O.6
[P]
O9
Mercury bioaccumulation into deep dwellers → food chain
D-O.6, D-O.7
[P]
O10
Particle feeders cannot feed in plume; food-web disruption
D-O.7
[P]
O11
Noise impact on marine mammals; mesopelagic food-supply reduction
D-O.8
[P]
O12
ISA mandate gap; no mining zones established
D-O.10
[P]
OSB-BL-071. Each O-item MUST carry: a verification status, an owner expectation, and a route (per UCFS Annex A pattern). None may be recorded as closed.
7 — Cross-cutting obligations for the building AI
OSB-BL-080. Do NOT upgrade verification status. Every DSM science/policy item is [P]. The building AI MUST NOT record any DSM claim as closed or any evidence as E3 without an independent verifier (none exists yet).
OSB-BL-081. Requirement IDs. Use OSB-BL-<nn> for this brief's items and propose UCFS-O-<area>-<nn>, ARCVB-O-<area>-<nn>, IAAP-O-<area>-<nn> for the DSM additions, each with a trace to the core clause it extends. One-to-one test-assertion design (ARCVB convention).
OSB-BL-082. Open-items register. Create/extend an open-items annex for DSM (parallel to UCFS Annex K, ARCVB Annex E, IAAP Annex B). Seed with: dark-oxygen primary-text verification; ISA Mining Code current draft status; whether bounded DSM claims in NW-O domains are legally permissible (mirror MASS K8); Oracle governance (who owns NOAA/ISA feed integrity).
OSB-BL-083. Lineage declaration. Every build MUST record what changed, what was carried forward, and what was NOT silently dropped (per UCFS Annex L, ARCVB Annex F, IAAP Annex C pattern).
OSB-BL-084. Version discipline. Determine before writing whether these additions are a defect correction or a substantive revision under UCFS §28.5. Adding DSM domains is a substantive revision — flag the annual-cadence implication (UCFS §28.5.2 single-cycle ended at v0.3). Record the decision in the revision log. [P] whether the IMO/ISA experience-building window argues for faster cadence (mirror IAAP B-11).
8 — Do-NOT-do list (hard constraints)
OSB-BL-090. MUST NOT renumber MASS domains D-A…D-N or MASS clauses that ARCVB Annex B and IAAP §6.1 reference.
OSB-BL-091. MUST NOT present any DSM engineering fix (plume filtration machine, "spit out water only", return-plume-to-seafloor) as validated, closed, or E3. They are [P] bounded fallbacks or open residues.
OSB-BL-092. MUST NOT claim court admissibility, ISA approval, or environmental compliance for any DSM artifact (mirror UCFS §21.3, §1.4.4).
OSB-BL-093. MUST NOT treat NOAA/ISA as counterparties in IAAP; they are Oracles (data) and/or regulators depending on function. Keep the distinction explicit.
OSB-BL-094. MUST NOT merge the three incoming updated files with this build list in one un-traced pass. Merge first, re-trace, then apply.
9 — Execution order for the building AI
Merge the three incoming updated files; run the re-trace (UCFS clause numbers → ARCVB Annex B → IAAP §6.1).
Classify each incoming change as defect-correction vs substantive (UCFS §28.5).
Verify [P] and open-item integrity across the merge.
Apply OSB-BL §2 (OSB layer doc).
Apply OSB-BL §3 (UCFS DSM domains + NW-O + evidence tiers).
Apply OSB-BL §4 (ARCVB Oracle service + DSM runtime monitors).
Apply OSB-BL §5 (IAAP ISA/mining counterparty cells).
Apply OSB-BL §6 (DSM friction map from 2025 notes).
Write lineage declaration + open-items register + revision log.
Report any item that could not be built and why (no silent drops).
