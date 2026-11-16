# THE MASS REGULATORY BRIDGE

**Guidelines for the Harmonized Application and Cross-Referencing of IMO Instruments Applicable to Maritime Autonomous Surface Ships**

**v0.6 — STANDALONE CONSOLIDATED WORKING DRAFT (GAO FUSION; VERIFICATION ROUNDS 1–2)**

| Field | Value |
| --- | --- |
| Date | 10 November 2026 (build date; see J6 item 1 for the date discrepancy with the Round 3 audit record) |
| Author / Architect | Sheldon K. Salmon |
| Status | PRIVATE ANALYTICAL GUIDANCE — NOT AN IMO INSTRUMENT |
| Supersedes | MASS Regulatory Bridge v0.1, v0.2, v0.3, v0.4, v0.5, v0.5.1 and v0.5.2, and the MRB v0.4 Amendment File (all retired as working drafts; see Part J) |
| Audit status | EXIT: UNAUDITED — v0.6 is v0.5 plus verification rounds 1 and 2 (Part M), done by the producing session against public web sources and one primary Coast Guard document. It narrows or corrects some items and is not an independent audit. Citations carried from v0.4 were not re-checked except where Part M says so |
| Standalone rule | This document is complete without v0.1, v0.2, v0.3, v0.4, v0.5, v0.5.1, v0.5.2 or the amendment file. All 30 core friction rows, 8 supplemental rows, 20 gaps, 7 BR findings, 14 corrections, 10 RT amendments, 4 insights, 16 GAO fusion items, 22 ground-truth items, 21 verification records and 22 closure dispositions are carried here. Deliberate removals, supersessions and fusion reconciliations are listed in Part J. |

## DOCUMENT MAP

- Part A — Control: A1 Build State · A2 Authority and Scope · A3 Source Register and Tags · A4 Glossary
- Part B — Structural Read (SG v1.0): B1 Declaration · B2 Substrate · B3 Agency · B4 Plan Primitives · B5 Risks · B6 Axes and Register · B7 Preservation and Invariant-Testing · B8 Greimas Fifth Position · B9 Closure Markers · B10 Gap Map
- Part C — Cross-Reference Matrix: C0 Index · C1 COLREG ↔ MASS (#1–#12) · C2 SOLAS/ISM/ISPS/STCW ↔ MASS (#13–#19) · C3 MARPOL ↔ MASS (#20–#24) · C4 Inter-instrument, case-law and national-law (#25–#30) · C5 Supplemental (S-1–S-8)
- Part D — Gap Register: G-1 to G-20
- Part E — Invariant Set (with the MASS 6.2 Framing Principle)
- Part F — Connection to Heterogeneity Under Observability (HET): F1–F6
- Part G — Red-Team and Correction Record: BR-01–BR-07 · C-01–C-14 · RT-01–RT-10 and Insights A–D · GF-01–GF-16 (G4)
- Part H — Ground Truth Ledger: GTL-01–GTL-22
- Part I — Peer-Review Readiness and τ Self-Check
- Part J — Lineage and Consolidation Record: J1–J11
- Part K — Approval Basis Interpretation Layer (ABIL) and S-5 Rule-Switching Specification: K1–K5
- Part L — GAO Fusion: Evidence and Structural Analogues (v0.5): L1–L5
- Part M — Verification Log (rounds 1–2, v0.6): M1–M5

## PART A — CONTROL

### A1. BUILD STATE

| Field | Value |
| --- | --- |
| Document | MASS Regulatory Bridge v0.6 |
| Purpose | Map structural friction between SOLAS 1974, COLREG 1972, MARPOL 73/78, and the non-mandatory MASS Code MSC.595(111), with grounded evidence, proposed resolutions, epistemic tags, and declared limits suitable for external peer review after independent verification. |
| τ | A maritime-law reader or MASS system designer who has not seen this document can locate at least 10 structural friction points between legacy IMO instruments and the MASS Code, each with cited evidence, a proposed resolution, and an epistemic tag, and can identify at least one claim that is wrong, overstrong, or requires external verification. |
| Round count | 3 of 3 audit rounds were completed at v0.4 (v0.1 was round 1; v0.2 applied the audit and red-team corrections; v0.3 consolidated both; the Round 3 fresh-context red-team audit produced RT-01 to RT-10, fused in v0.4). v0.5 is an Architect-directed source-extension build (GAO fusion), not an audit round; see J6 item 11. |
| Open findings | v0.1 BR-01 to BR-07 dispositioned (Part G). v0.2 corrections C-01 to C-14 carried. Round 3 amendments RT-01 to RT-10 applied (G3). GAO fusion items GF-01 to GF-16 applied (G4). Verification records VR-01 to VR-21 applied (Part M). Ground-truth ledger dispositions (M5): 5 closed-verified, 3 closed-rescoped, 5 open-doable, 9 open-external. Fresh-context audit of v0.6 pending. |
| Status | IN CYCLE — verification round 2 applied; closure dispositions set (M5); audit pending |
| Advancement | Clear the five open-doable ledger items (M5), then a fresh-context audit of the result by an independent reviewer. The nine open-external items are declared limits that need the Architect’s own source files or outside work. A further round needs Architect direction, or a declared new question if the purpose or τ changes. |
| Stop condition | τ test passed under fresh-context review, or Architect stop. Round 3 completion was reached at v0.4 (see J6 item 2). |

### A2. AUTHORITY AND SCOPE

1. This document is a private structural and regulatory analysis. It is not an IMO instrument, not legal advice, not a flag-state circular, not a recognized organization rule, and not a certification basis by itself. [D-BP / R]

2. The MASS Code, MSC.595(111), was adopted on 21 May 2026 and invited Governments to give effect to it on 1 July 2026. It is expressly non-mandatory until made mandatory through a future instrument. [D-MSC Res. §§1–3; MASS 1.2.4]

3. The roadmap annexed to MSC.595(111) expects the mandatory MASS Code to enter into force on 1 January 2032 through SOLAS Chapter XVI. That date is a roadmap target, not current law. [D-MSC Annex 17; R] v0.5 note: GAO-24-107059 (p. 7), reporting IMO expectations as of May 2024, gave the same mandatory-effect year (2032) and a non-mandatory adoption target of 2025; the Code was adopted in May 2026 per D-MSC, so the non-mandatory step came about a year later than that 2024 expectation while the 2032 target is unchanged in the supplied sources. [D-GAO24 p. 7; D-MSC; R] v0.5.1 verification (VR-02): IMO-side summaries state that the mandatory Code is planned to enter into force on 1 January 2032 at the earliest and that this timeline may need to be revisited, and that a MASS working group is to be re-established at MSC 112 in December 2026 to frame the experience-building phase. [D-IMO; R]

4. During the 2026–2032 transition, the mandatory legal baseline remains the applicable SOLAS, COLREG, MARPOL, flag-state, coastal-state and port-state requirements. The MASS Code functions as voluntary guidance unless made binding by national implementation or other legal action. [D-MSC 1.2.4; D-SB treaty status; R]

5. The MASS Code applies to cargo ships to which SOLAS chapter I applies, including associated ROCs, when the Administration deems compliance with other applicable instruments impracticable or insufficient. It excludes cargo high-speed craft to which SOLAS chapter X applies and warships, naval auxiliaries, and other government non-commercial ships. [D-MSC 2.1]

6. The invitation to apply the MASS Code to MASS below 500 gross tonnage is phrased “as far as practicable” and creates no mandatory small-MASS regime. [D-MSC Res. §3]

7. COLREG amendment freeze window (v0.4, Insight C). COLREG was last amended in 2013 (A.1085(28)). [D-SB COLREG entries (1)–(7)] No further amendment cycle is scheduled in the supplied sources [?], the Art. VI route is slow (see B2), and the roadmap target for the mandatory MASS Code is 1 January 2032. [D-MSC Annex 17] Read together, COLREG text is practically frozen for about five years of the 2026–2032 transition. This is a practical freeze, not a legal one: an Art. VI amendment remains possible. [R] Consequences: (a) MASS–COLREG harmonization during the window must occur through interpretation, not amendment; (b) flag states have until about 2032 to develop interpretive frameworks; (c) the first flag states to approve MASS with robust COLREG interpretations may set de facto global practice [S]; (d) the ABIL (Part K) becomes the primary vehicle for COLREG interpretation during this window. [R; S] The window could change if an extraordinary COLREG amendment cycle is convened. [D-SB; D-MSC Annex 17; R; S] v0.5 GAO corroboration (GF-02): GAO-24-107059 (p. 13) reports Coast Guard officials saying that IMO determined autonomous ships must still meet the COLREG look-out requirement and that the international regulation need not be amended at this time, so each country must decide how autonomous ships comply; it also reports that the Coast Guard has no present plan to change its domestic regulations or publish autonomous-ship policy guidance before the IMO framework exists. Both are officials’ statements as reported by GAO in mid-2024, not the IMO record (GTL-18). They fit the practical-freeze reading and do not make it a legal freeze. [D-GAO24 p. 13; R; ?] v0.6 verification (VR-16): the IMO scoping outcome itself (MSC.1/Circ.1638, Table 3) classes COLREG as a high-priority instrument and gives option I (equivalence or interpretation) for degree one, I–II for degrees two and three and II (amend) for degree four. A “no amendment at this time” position is therefore a later IMO decision, not the 2021 scoping outcome; it is reported by GAO-24 but has not been traced to the MSC record (GTL-18). [D-IMOP; D-GAO24 p. 13; ?]

8. Domestic statutory baseline (added v0.5, GF-01). The “flag-state … requirements” in item 4 include domestic statutes written on the assumption that people are aboard. GAO-24-107059 (pp. 2, 10, 12) reports, for the United States, statutes that fix minimum crew and require credentialed masters, mates and watchmen, U.S. citizens in certain officer roles, and a pilot, and the Coast Guard’s position that it cannot waive them for autonomous ships outside the statutorily directed at-sea rocket-recovery pilot. Other flag states’ statutes are unsurveyed. This layer is mapped as friction #29 and gap G-16, and it bears directly on the crew-reduction premises of the MASS Code. [D-GAO24 pp. 2, 10, 12, fn. 21–23; R; ?]

Reading convention. Wherever this document says the MASS Code “requires” something, read it as “requires, as guidance, unless made binding by national implementation” until SOLAS Chapter XVI is in force. The authority of this analysis rests on the mandatory instruments (SOLAS, COLREG, MARPOL); the MASS Code is treated as guidance, not law. [D-MSC 1.2.4; R]

### A3. SOURCE REGISTER AND TAG DISCIPLINE

| Code | Source | Use in this document | Limit |
| --- | --- | --- | --- |
| D-MSC | MSC.595(111), MASS Code, Annex 16; Annex 17 roadmap | Direct MASS Code text, dates, scope, chapters, paragraphs, EPs | Non-mandatory until future mandatory adoption |
| D-SB | Status of IMO Treaties, Volume I, 30 October 2026 | Treaty status, amendment entries, final clauses, depositary information | Status Book says it is “for information only” and does not replace official communications |
| D-SG | Structural Grammar v1.0 | Read method, tags, rungs, markers, Invariant-Testing, limits | SG v1.0 is unaudited; 39-system evidence base; mostly one-reader corpus |
| D-BP | Build Protocol v1.0 | Purpose, τ, Build State, round cap, audit separation | BP’s SG summary is older than SG v1.0; SG v1.0 controls grammar details |
| D-HET | Heterogeneity Under Observability | Adversary classes, H_d_variant, hidden centralization, COLREG excerpts | HET protocol is proposed, not run; external references not independently verified here |
| D-UKSC | Evergreen Marine (UK) Ltd v Nautical Challenge Ltd [2021] UKSC 6 (the “Ever Smart” case) | Holding on Rule 9 versus the crossing rules (para 145), the no-steady-course holding (paras 111–112), the Rule 17 triggers (paras 60–61), the Maloja II timing statement (para 40), and COLREG text as quoted in the judgment | UK Supreme Court: binding in UK law, persuasive elsewhere. The Round 3 audit recorded verification against the full judgment; the judgment was not re-opened in the v0.4 or v0.5 fusions. |
| D-GAO22 | GAO-22-104567, Uncrewed Maritime Systems: Navy Should Improve Its Approach to Maximize Early Investments (7 April 2022) | U.S. Navy cost, governance, prototyping, certification and digital-infrastructure findings; used for G-8 scale, G-19, F6, S-7 and as a structural analogue (L4) | Military programme audit; figures and Navy positions date from 2020–2022; not a regulatory source; cited by printed page |
| D-GAO24 | GAO-24-107059, Coast Guard: Autonomous Ships and Efforts to Regulate Them (8 August 2024) | IMO autonomous-ship process as of mid-2024; Canada, Norway and UK approaches; U.S. Coast Guard authority, practice and stated challenges; stakeholder views | Predates MSC.595(111); U.S.-centred; IMO and Coast Guard positions are officials’ statements as reported by GAO; Japan and South Korea did not respond (p. 16); stakeholder quantifiers follow GAO’s convention (most 13–16, many 8–12, some 5–7, a few 3–4 of 17; p. 15); cited by printed page |
| D-GAO26 | GAO-26-109014, Robotic Autonomous Systems: Navy Needs to Address Leadership and Organizational Challenges to Meet Urgent Needs (15 June 2026) | Navy robotic autonomous systems (RAS) leadership, organization and development-approach findings; unclassified summary of a March 2025 classified report | Omits classified detail; reports March 2025 findings, partly overtaken by later Navy and statutory changes noted in its own footnote 5; cited by letter page or Snapshot |
| D-IMO | IMO web pages: MSC 111 meeting summary (13–22 May 2026) and MASS FAQ page, with class-society and trade summaries used only as corroboration | MASS Code adoption, effect date, non-mandatory status, experience-building phase, roadmap, other committees’ MASS work | Web summaries, not the resolution text; adoption-day stamp and Annex 17 not re-read; secondary summaries differ on the adoption day (21 or 22 May) |
| D-USC | 46 U.S.C. § 8301 as in force on 23 December 2025, read on uscode.house.gov and in the 2024 GovInfo edition | Scope and exceptions of the U.S. minimum-licensed-individuals statute | Other Title 46 sections cited in #29 not read; later amendments not checked |
| D-USCG-WI | U.S. Coast Guard CG-5P Work Instruction 5P-WI-002(1), Oversight of Unmanned, Autonomous and Remote-Control Operations (original date 1 June 2026) | Current Coast Guard guidance to Captains of the Port and Officers in Charge, Marine Inspection; cancels Policy Letter 22-01 (Change 1); manning floor; COLREGS compliance statement | Non-binding by its own disclaimer; covers unmanned maritime systems and testing on inspected vessels, not the MASS Code; read in full in v0.5.1 |
| D-GAO26T | GAO-26-108762, Coast Guard: Approaches to Autonomous Ship Regulation (testimony to a House subcommittee, December 2025) | Refresh of GAO-24 on the Coast Guard position as of December 2025 | Read only through search excerpts in v0.5.1, not in full |
| D-TC | Transport Canada Tier I Policy TP 13585, Oversight of Small Maritime Autonomous Surface Ships (effective 1 February 2022), read through search excerpts | Canadian small-MASS scope and approval route | Excerpts only; annexes and the separate Tier I policy on autonomous navigation systems not read |
| D-UKSI | UK Merchant Shipping (Small Workboats and Pilot Boats) Regulations 2023, SI 2023/1216 (in force 13 December 2023), read through legislation.gov.uk excerpts; Workboat Code Edition 3 Annex 2 known only through law-firm summaries | UK definitions and scope for remotely operated unmanned vessels under 24 m | Annex 2 text not read; summaries are secondary |
| D-IMOP | IMO primary documents read in round 2: Resolution MSC.595(111) (cover and contents pages, via search excerpts) and MSC.1/Circ.1638 (annex pages 1–66 read) | Adoption date; scope and Table 3 of the regulatory scoping exercise | MASS Code body not re-read; Circ.1638 annex pages 67 onward, including the COLREG appendix, not read |
| D-DOD | U.S. Department of Defense releases NR-448-16 (16 December 2016) and NR-451-16 (19 December 2016), and the 20 December 2016 statement on the return | Glider seizure and return | Official statements; trade and news reports corroborate |
| D-NMA | Norwegian Maritime Authority circular RSV 12-2020 (27 August 2020) on sdir.no, read in excerpts; NMA presentations to IMO (MSC 108 INF.16; 2024 symposium) | Norwegian approval approach; Yara Birkeland crew | Excerpts only; the circular’s planned revision not read |
| R | Derived inference | Derived from at least two D points with a stateable inference step | Not direct text |
| S | Judgment / external memory / proposed design rule | Extrapolation, model memory, non-in-context law, engineering proposal | Requires verification before reliance |
| ? | Open / unverified | Missing source, unresolved legal detail, future regime | Not a finding of fact |

Combined tags: [S/GTL] = judgment or recalled external text that is also listed in the Ground Truth Ledger (Part H). [GTL] alone = the claim depends on a Part H verification item.

Critical source limitation. The provided SOLAS/COLREG/MARPOL source is the Status Book, not the consolidated operative text of every regulation or rule. It verifies treaty status, amendment lists and reproduced final clauses. It does not reproduce all SOLAS regulations, all COLREG Rules, or all MARPOL Annex provisions. [D-SB; R] Therefore:

- MASS Code citations are directly checkable as [D-MSC].
- SOLAS/COLREG/MARPOL amendment counts and final clauses are directly checkable as [D-SB].
- Operative rule text quoted in HET is directly checkable as [D-HET], but not independently verified against the official COLREG consolidated text here.
- Operative SOLAS/COLREG/MARPOL details not present in the provided sources are tagged [S] or [?] and placed in the Ground Truth Ledger.
- UKSC citations are checkable as [D-UKSC] against the judgment. Paragraph numbers are carried from the Round 3 audit and have not been re-checked in v0.4 or v0.5. [D-UKSC; R]
- GAO citations are checkable as [D-GAO22], [D-GAO24] and [D-GAO26] against the three supplied PDFs and were checked in the v0.5 build. They are GAO’s account of what officials and stakeholders told it, not primary instruments. Statutes, cases, policy letters and IMO documents that GAO cites are not checked here (GTL-17 to GTL-22). [D-GAO; R]

SG/BP version conflict. BP v1.0 describes SG as having “twenty-seven read markers, three read kinds, composition rules, epistemic mechanisms, and a purpose metric.” [D-BP §F.1] SG v1.0 states 26 read markers, 2 read kinds, and that the purpose metric is staged, not part of v1.0. [D-SG §0.3, §XXV, §XXXIII] This document uses SG v1.0 for structural-read rules and BP v1.0 for governance. Where they conflict, the full SG v1.0 specification controls the grammar. [R]

### A4. GLOSSARY

Expansions are standard usage [S] unless a MASS Code paragraph is cited.

| Term | Meaning | Where used |
| --- | --- | --- |
| MASS | Maritime Autonomous Surface Ship | throughout |
| ANS | Autonomous Navigation System; navigation without human intervention under specified conditions [D-MSC 4.3] | B3, C1 |
| ROC | Remote Operation Centre | B3, C1–C3 |
| ROCSMS / ROM DoC / RMC | ROC Safety Management System / Document of Compliance for the Remote Operation Management company / ROC Management Certificate [D-MSC 11.3] | #18 |
| OE | Operational Envelope [D-MSC 8.3.1] | #3, #4, #9 |
| ODD | Operational design domain (autonomy-field term used alongside OE) [S] | B5, #3 |
| ConOps | Concept of operations [D-MSC 8.2] | C1 |
| SCS | Stability Control System [D-MSC 19.2.2] | #14 |
| SSP / SSO | Ship Security Plan / Ship Security Officer | #17 |
| V&V | Verification and validation | C1 |
| CPA / TCPA | Closest point of approach / time to CPA | #7 |
| TSS | Traffic separation scheme | #6 |
| AIS / VDES / VDR / ECDIS | Automatic Identification System / VHF Data Exchange System / Voyage Data Recorder / Electronic Chart Display and Information System | #5, #13 |
| IOPP | International Oil Pollution Prevention certificate | #20 |
| III Code | IMO Instruments Implementation Code (mandatory via SOLAS Ch. XIII) | #27 |
| HSSC | Harmonized System of Survey and Certification | B4 |
| DOF | Degree of freedom (HET term; apparent vs genuine) | #7, Part F |
| H_d_variant | HET variant-fraction measure; see Part F | Part F |
| k_cap | HET quantity for topology-adjusted capture; working gloss: how many MASS one compromised ROC or shared channel can reach [D-HET §4.6 Scene 5; R] | Part F |
| GTL | Ground Truth Ledger (Part H) | throughout |
| ABIL | Approval Basis Interpretation Layer (this bridge’s term; not in MSC.595(111)) [R; S] | Part K, #25, S-5 |
| UKSC | United Kingdom Supreme Court; here Evergreen Marine (UK) Ltd v Nautical Challenge Ltd [2021] UKSC 6 (“Ever Smart”) | #25, #28, S-5 |
| ENC | Electronic navigational chart | S-5, K4 |
| MSMD | Minimum safe manning document (assumed expansion [S]; used in K2 #19 without a definition in the source files; J6 item 6) | K2 |
| RAS | Robotic autonomous systems (GAO-26 usage; military context) | L, F6 |
| USCG / COTP | U.S. Coast Guard / Captain of the Port, the Coast Guard officer directly responsible for law enforcement in a designated area [D-GAO24 p. 10, fn. 11] | #29, K1, L3 |
| AutoPoCo | Automated and Autonomous Vessel Policy Council, a Coast Guard internal advisory committee chartered 22 June 2021 [D-GAO24 p. 11] | L3 |
| IMO degrees of autonomy | Four degrees proposed by IMO in 2018: (1) automated processes and decision support, crew aboard; (2) remotely controlled with crew aboard; (3) remotely controlled without crew aboard; (4) fully autonomous [D-GAO24 pp. 3–4, Fig. 2] | #29, L2 |
| PAE | Portfolio acquisition executive, the Navy official leading a portfolio of capabilities (10 U.S.C. § 1732 as reported in GAO-26 fn. 5; not checked) | L4 |

## PART B — STRUCTURAL READ (SG v1.0 APPLIED)

### B1. READ DECLARATION

| Field | Value |
| --- | --- |
| Target_1 | Structural friction between legacy IMO instruments and the MASS Code |
| Read target | System |
| Read scope | Instance |
| Order | 2 |
| Assertion | Assertive / Speculative where marked |
| Readable scope | Partially readable as a regulatory-system instance |

The system is readable because it has a definable regulatory/informational substrate, definable states at treaty adoption, amendment and implementation moments, and separable markers: instruments, provisions, agencies, compliance mechanisms, risks and gaps. [D-SG §XX.5; D-MSC; D-SB; R] The read is partial because the operative texts of many SOLAS, COLREG and MARPOL provisions are not supplied in full, and flag-state implementation is not surveyed. [D-SB; R]

### B2. SUBSTRATE

| Instrument / process | Substrate type | Count | Temporal position | Shape | Evidence |
| --- | --- | --- | --- | --- | --- |
| SOLAS 1974 | Regulatory + Informational | Single instrument family | Present; amendments listed through MSC 111, 2026 | Flat / layered | Status Book lists SOLAS amendment entries (1)–(223). [D-SB] |
| COLREG 1972 | Regulatory + Informational | Single instrument family | Present; seven amendment entries, last 2013 | Flat / layered | Status Book lists COLREG amendments (1)–(7). [D-SB] |
| MARPOL 73/78 | Regulatory + Informational | Plural annex/protocol structure | Present; 1978 Protocol entries (1)–(90); 1997 Protocol entries (1)–(29) | Flat / layered | 90 MARPOL 1973/1978 entries and 29 MARPOL PROT 1997 entries. [D-SB] |
| MASS Code MSC.595(111) | Regulatory + Informational | Single code | Adopted 21 May 2026; effect invited 1 July 2026; non-mandatory | Goal-based / layered | Res. §§1–3; MASS 1.2.4. [D-MSC] |
| IMO committee / amendment process | Regulatory procedural mechanism | Process, not co-equal treaty | Present | Recursive procedural layer | SOLAS Art. VIII, COLREG Art. VI, MARPOL Art. 16 reproduced in Status Book. [D-SB] |

**COLREG amendment procedure (corrected and expanded, RT-05).** COLREG Art. VI, as reproduced in the Status Book, establishes a four-stage procedure, distinct from SOLAS Art. VIII tacit acceptance: [D-SB COLREG Art. VI]

1. Proposal and circulation: an amendment is proposed by a Contracting Party, submitted to IMO and circulated to all Contracting Parties and Members at least six months before consideration.
2. MSC adoption: the amendment is referred to the MSC and adopted by a two-thirds majority of those present and voting in the MSC.
3. Assembly adoption: the amendment is communicated to all Contracting Parties for acceptance and adopted by a two-thirds majority of those present and voting in the Assembly.
4. Entry into force: on a date determined by the Assembly, unless more than one-third of Contracting Parties notify objection by a prior date determined by the Assembly.

The last COLREG amendment (A.1085(28), 2013) took this route. [D-SB] Any MASS-specific COLREG amendment would face this full procedure, which is slower and more politically exposed than SOLAS amendments. COLREG text is therefore practically frozen for MASS until at least 2032 (A2 item 7); this is a practical, not a legal, freeze. All MASS–COLREG harmonization during 2026–2032 should occur through flag-state approval, ConOps declarations, the regulatory gap analysis and the approval basis (Part K), not through COLREG amendment. [D-SB; D-MSC Ch. 6, Annex 2 §8.2; R]

Substrate plurality: Plural. The system consists of multiple instruments plus amendment and approval mechanisms. The IMO committee process is a procedural mechanism, not a fifth treaty substrate. [R]

National implementation layer (added v0.5, GF-01, GF-06). Between the instruments and the vessel sits a national layer that earlier versions treated only as “flag-state implementation”: domestic statutes and the administering agency’s practice. GAO-24-107059 shows what that layer can contain in one flag state: statutory minimum-crew and credential rules that the Coast Guard says it cannot waive outside one pilot, regulations on automated systems last written in 1987–88, equivalency and case-by-case testing guidance, and local Captain of the Port discretion (pp. 10–13). This layer is not a fifth treaty substrate and not an IMO instrument; it is where the voluntary-to-mandatory transition (T2) is in practice decided for a given ship. Its content for flag states other than the United States is unsurveyed (GTL-15, GTL-17). [D-GAO24 pp. 10–13; R; ?]

History: Present. Amendment histories are reproduced in the Status Book. [D-SB]

Relation: Present. The MASS Code declares itself “supplementary to any other applied instruments” [D-MSC 1.2.1] and “required to conform to the relevant rules of international law” [D-MSC Preamble 6]. The instruments are coupled through shared definitions (terms not defined in the Code take SOLAS definitions [D-MSC 4]), harmonized survey and certification [D-MSC 5.2.1], SOLAS/COLREG navigation compliance [D-MSC 16.2], and shared purpose (safety of navigation, pollution prevention). [R]

### B3. AGENCY

| Agent | SG mode | Faces present | Location | Evidence / limit |
| --- | --- | --- | --- | --- |
| IMO MSC / MEPC / Assembly | Merged institutional | Intent, Observation, Capacity, Commitment | Institutional | SOLAS Art. VIII, COLREG Art. VI, MARPOL Art. 16. [D-SB] |
| Contracting Governments / Parties | Plural / distributed | Intent, Commitment, Capacity | National / international | Treaty acceptance and objection mechanisms. [D-SB] |
| Administration | Single / institutional | Intent, Observation, Capacity, Commitment | Flag state / approval authority | MASS 2.1, 5, 6, 14. [D-MSC] |
| Human master, conventional vessel | Single | All five faces | On board | Traditional COLREG / SOLAS model. [S/GTL] |
| Human master, MASS | Single at any given time; may be successional | All five faces | On board or ROC; if persons on board, master physically on board | MASS 14.2.1.10–.14. [D-MSC] |
| Remote operator | Single per assigned watch / task; plural across ROC | All five faces | ROC | MASS 4.32, 14.2.2. [D-MSC] |
| Autonomous Navigation System | Contingent / capacitive system | Observation and Capacity present; Intent, Commitment, Utility absent in the SG sense | On board / integrated system | MASS 4.1, 4.3, 8.7.3, 14.2.1.10 (see the asymmetry note below). [D-MSC; R] |
| Company / ISM Company / ROM company | Merged institutional | Intent, Commitment, Capacity | Shore / company / ROC | MASS 5.7, 11.2, 11.3. [D-MSC] |

Key agency finding. The ANS has Observation and Capacity but not Intent, Commitment or Utility: it can sense and act but has no wants. This is the same face-split pattern as the SG’s Matrix Construct. [D-SG §III, Rung 4; R] The ANS is not a legal master. The MASS Code preserves a human master and human oversight: “There should be a human master responsible for a MASS, regardless of the mode of operation and the master should have the means to intervene when necessary.” [D-MSC 8.7.3; also 4.3, 8.7.1–8.7.4, 14.2.1.10–.14]

**ANS entry — agent/responsibility asymmetry (RT-10).** MASS 4.1 defines “Agent” to include software: “Agent means a human or software (computer or computer system(s)) responsible for performing or supervising control actions.” [D-MSC 4.1] But MASS 8.7.3 reserves the master role for humans: “There should be a human master responsible for a MASS.” [D-MSC 8.7.3] And MASS 14.2.1.10: “Regardless of the mode of operation, the master is responsible for the safe operation of the MASS at all times.” [D-MSC 14.2.1.10] The MASS Code uses “agent” in a cybernetic sense (software can be an agent) but reserves legal responsibility for humans. The ANS is an agent under 4.1 but not a master under 8.7.3. This asymmetry is the legal foundation of the bridge: the ANS acts, but the human is responsible. [D-MSC 4.1, 8.7.3, 14.2.1.10; R]

Correction carried from v0.1. The master may be at a ROC, but if crew or persons are on board, MASS 14.2.1.12 requires the master to be physically on board. [D-MSC]

Agency failure modes (restored from v0.1; classification is [R], citations [D-MSC]):

| Agency mode | Failure | Trigger | Evidence |
| --- | --- | --- | --- |
| Single | Usurped | Cyber intrusion seizes ANS control | MASS 9.8, 12.3.2 |
| Merged (master + ANS) | Fractured | Master loses situational awareness during handover | MASS 8.7.4 |
| Contingent (ANS depends on ROC connectivity) | Orphaned | Connectivity lost; ANS enters fallback state | MASS 8.4, 17.2.9 |
| Self-referential (ANS monitors its own performance) | Fractured | Systematic failure undetected | MASS 4.37 |

v0.5 additions (GF-04, GF-06, GF-08). (1) IMO working-group positions. GAO-24-107059 (p. 7) reports the IMO joint working group agreeing that an autonomous ship should have a human master, aboard or remote, who can take control; that a ship may have several masters over one voyage but only one remote operating centre responsible at any one time; and that a master may be responsible for several ships in some circumstances. These agree with the single-at-any-time, possibly successional master mode in the Agency table above and sharpen it: the one-ROC-at-a-time rule is a handover rule, and the several-ships-per-master allowance is a workload and k_cap issue (F5, G-7). They are working-group agreements as reported in 2024, not MASS Code text. [D-GAO24 p. 7; R] (2) Administration plurality in practice. The Administration row above is classified Single / institutional. For the United States, GAO-24 (pp. 10–11) describes approvals made case by case by local Captains of the Port, with headquarters working to give them a common risk-assessment framework after industry raised consistency concerns. In that flag state the Administration function is in practice spread across ports, which is closer to a Plural / distributed reading. This is an inference from one flag state. [D-GAO24 pp. 10–11; R] (3) Handover as a failure site. A few stakeholders were concerned about technical difficulty when control passes between humans and autonomous systems (GAO-24 p. 5), a stakeholder-reported example of the Fractured failure mode for merged master + ANS agency. [D-GAO24 p. 5; R]

### B4. PLAN PRIMITIVES

| Primitive | Instance in regulatory bridge | State / mode | Evidence |
| --- | --- | --- | --- |
| Container | Ship classes, MASS category, certificates, records, ConOps, OE, ODD | Present | MASS 2, 4, 5, 8. [D-MSC] |
| Transform | Conventional obligation → autonomous/remote functional equivalent; amendment; approval | Present | MASS 6, Annex 1; SOLAS/COLREG/MARPOL amendment clauses. [D-MSC; D-SB] |
| Bound | Scope limits, OE/ODD, exclusions, fallback thresholds, certificate validity | Present | MASS 2, 5.6, 8.3–8.5. [D-MSC] |
| Connect | MASS ↔ ROC ↔ Company ↔ Administration ↔ third parties | Present | MASS 17, 18, 11, 12. [D-MSC] |
| Recurse | Approval → operation → data → review → modification → reapproval; treaty amendment loop | Direct; balancing intended, reinforcing risk remains | MASS 6.4.2, 8.2.5, 9.10; Status Book amendment histories. [D-MSC; D-SB; R] |
| Synchronization | HSSC survey harmonization; voyage phases; watch handover; amendment timing | Present but desynchronized across instruments | MASS 5.2.1, 14.2.1.15, 18.2.5; Status Book amendment dates. [D-MSC; D-SB; R] |

Primary element: Recurse (Direct, Balancing intended). The instrument set is self-referential: amendments are produced by the same body (MSC/MEPC) that produces the original instruments, the MASS Code requires compliance with the instruments it supplements, and the regulatory gap analysis feeds back into approval. The bridge depends on feedback from operation and approval back into rulemaking, ConOps, risk assessment and certification. The loop is balancing to the extent amendments correct gaps (COLREG amended 7×, SOLAS 223×, MARPOL 90×). [D-SB; R] It is not proven that the loop is always balancing; amendment accumulation can also create reinforcing complexity. The 223:7 SOLAS-to-COLREG entry ratio (about 32:1) suggests COLREG may be under-amended relative to operational change. [D-SB; R]

### B5. RISKS

| Risk | Paired primitive | State | Evidence | Resolution direction |
| --- | --- | --- | --- | --- |
| Unrated | Container | Live | Small MASS below 500 GT addressed only by invitation “as far as practicable.” [D-MSC Res. §3] | National small-MASS rules or future IMO instrument |
| Unfalsifiable | Transform | Live | “Adequate situational awareness,” “ample time,” and “scanty information” need operational thresholds. No test exists for whether an ANS’s Rule 2 departure decision was justified; MASS 8.7.3 requires master intervention ability but defines no threshold. [D-MSC 8.7.4, 16.4.2; D-HET Rule 7; R] | Declare measurable acceptance criteria in ConOps/V&V |
| Exempt | Bound | Live | Warships / government non-commercial ships excluded. Military autonomous vessels operate outside the framework. [D-MSC 2.1.2] | Separate military assurance regime; voluntary alignment |
| Coupled | Connect | Live | Connectivity degradation, ROC compromise and fallback are linked; a single connectivity failure can propagate. [D-MSC 12.4.3, 17.2.9] | Topology, redundancy, isolation, fallback validation |
| Open | Recurse | Live | Future mandatory regime remains projected; the roadmap may revise entry into force after maturity assessment. The amendment process is open-ended but bounded by tacit acceptance. [D-MSC Annex 17; D-SB] | Version-lock approval basis; monitor MSC roadmap |
| Desynchronization | Synchronization | Live | COLREG last amendment entry 2013; MASS Code 2026; SOLAS/MARPOL 2026 entries continue; COLREG and the MASS Code are 13 years apart in cycle. [D-SB; D-MSC] | Rule-version matrix and amendment horizon scan |
| Misapplied | Universal | Live | Human sensory terms and crew-based procedures applied to autonomous/remote systems without equivalence analysis; e.g., Rule 5 “sight and hearing” applied to sensor fusion. The Code resolves this through “situational awareness” [16.4.2] but the COLREG text is unchanged. [D-HET; D-MSC 16, 19–24; R] | Provision-level equivalence and verification mapping |

v0.5 GAO corroboration of existing risk labels (no new risk class is added to the SG read) [R]. **Exempt**: GAO-22 (pp. 3–5, 14) and GAO-26 (letter p. 1; Snapshot) describe a large military uncrewed-vessel effort outside the MASS Code; GAO-22 reports a December 2020 plan for 143 uncrewed vessels and vehicles among 546 total by 2045, a figure that is dated and not checked against later plans. **Unfalsifiable**: GAO-22 (pp. 26–27) found Navy prototypes without measurable criteria for when they are ready to move to acquisition, the same absence of acceptance criteria this bridge flags in #3, #4 and #7. **Desynchronization**: GAO-24 (p. 7) records IMO’s 2025 non-mandatory target, which the Code met in 2026 per D-MSC (A2 item 3). **Coupled**: GAO-22 (pp. 3, 23, 30) describes digital infrastructure common to all four major Navy efforts (F6). [D-GAO22 pp. 3–5, 14, 23, 26–27, 30; D-GAO24 p. 7; D-GAO26 p. 1; R]

### B6. AXES AND REGISTER

| Axis | Reading | Evidence / risk |
| --- | --- | --- |
| Rate | Amendment rates differ sharply: SOLAS 223 entries; COLREG 7; MARPOL 1978 Protocol 90 and 1997 Protocol 29. | [D-SB]. Desynchronization risk. |
| Cost | Verification cost rises with autonomy, ROC certification, cyber assurance, software V&V and multi-instrument compliance. | [D-MSC 5–10, 17–18; R]. Cost must be allocated across Administration, Company, ROM company and submitter. |
| Depth | Deep regulatory stack: treaty → annex/chapter → code → approval basis → ConOps → OE/ODD → software → data logging. | [D-MSC; R]. Wrong-depth risk: vessel-level proof cannot substitute for flag-state audit, and flag-state audit cannot prove a specific ANS maneuver. |

Register: Emergent, Mechanism: Structural. The felt quality is layered regulatory accretion without unified architecture. SOLAS was built for safety of life, COLREG for collision avoidance, MARPOL for pollution prevention; the MASS Code is the first instrument to bridge all three for a new vessel class. The emergent quality is “regulatory heterogeneity”: one operational reality (an autonomous ship at sea) governed by several instruments with different amendment cycles, compliance mechanisms and agency assumptions. [R] Register failure risk: Ungrounded, if the bridge treats voluntary MASS Code provisions as already mandatory law. [D-MSC 1.2.4; R]

### B7. PRESERVATION DECLARATION AND INVARIANT-TESTING

Declared anchor: Relation. What is preserved is the relational structure of maritime safety, security, environmental protection, responsibility, oversight and compliance obligations across the transition from conventional crewed operation to autonomous or remote functions. [D-MSC 1.2.2, 6.2, 8.7, 16.2; R] The anchor is not “same crew,” “same bridge,” or “same equipment.” It is that duties remain relationally assigned and assessable despite changed agents and substrates. The Code’s criterion is to “ensure a level of safety, security and environmental protection that is expected of a conventional ship.” [D-MSC 6.2]

| ID | Transformation | Observed / projected | Anchor effect | Evidence | Verdict |
| --- | --- | --- | --- | --- | --- |
| T1 | Adoption of non-mandatory MASS Code, 2026 | Observed | Relation retained as guidance: 16.2 requires SOLAS/COLREG compliance; 6.2 preserves conventional safety level | [D-MSC Res., 6.2, 16.2] | Retained, but non-mandatory |
| T2 | Transition period 2026–2032 | Observed / current | Relation degraded: Code guidance is voluntary unless implemented by the Administration; mandatory legacy duties remain | [D-MSC 1.2.4; D-SB; R] | Degraded |
| T3 | Mandatory Code via SOLAS Chapter XVI around 2032 | Projected | Relation expected to strengthen if the roadmap completes | [D-MSC Annex 17; S] | Not included in observed verdict |

Invariant-Testing verdict: PARTIAL for observed T1–T2. Confidence: MODERATE. The Relation anchor is retained in text but degraded in enforceability during the voluntary transition. No observed transformation in the supplied sources proves total loss of the anchor. [D-SG Mechanism 7; R] T3 is a projection and is not used to claim HOLDS. [S] The T2 degradation is this bridge’s primary target: between 1 July 2026 and the projected 1 January 2032, MASS operate under a voluntary code alongside mandatory SOLAS/COLREG/MARPOL. The regulatory gap analysis [D-MSC Annex 2 §8.2] is one integration mechanism among several (flag-state implementation, SOLAS certificates, equivalency/exemption documentation, ISM/ISPS, and approval). [R]

### B8. GREIMAS FIFTH-POSITION LIMIT

SG v1.0 records the Greimas fifth-position limit as confirmed 11 times. [D-SG §IX, §XVIII] This bridge is a candidate post-v1.0 instance, not an admitted twelfth SG confirmation. [R]

| Position | Regulatory reading |
| --- | --- |
| S1 | Conventional vessel: onboard crew, human bridge, legacy instruments |
| S2 | Fully autonomous vessel: no human intervention in specified functions |
| ~S1 | Not conventional: autonomous or remote functions present |
| ~S2 | Not fully autonomous in governance: human master / oversight persists |
| Fifth position | MASS: autonomy under human legal responsibility and Administration-approved operational context |

The fifth position is required because the substrate state “ship” and the agency state “distributed human-machine control” are orthogonal. [R]

### B9. REQUIRED SG CLOSURE MARKERS

| Marker | Declaration |
| --- | --- |
| Assertion Surface | Factual status: Assertive for sourced text; Hypothetical for proposed resolutions; Counterfactual only where the future mandatory regime is discussed. Commitment: Asserted for [D], Speculative for [S]. |
| Token presence | Existential tokens: specific MASS provisions, Status Book entries, UKSC paragraphs, HET concepts. Universal claims are limited to “within cited instrument scope,” not global claims over all flag states. |
| Anti-Hegemonic Check | Sourcing axis: IMO treaty law, Western/international maritime regulatory practice, SG/HET author-owned frameworks, and one UK Supreme Court judgment (a single-jurisdiction common-law source). Coverage type: transmission / institutional internationalization, not independent cross-civilizational discovery. Flag fires: single institutional tradition. v0.5 adds three U.S. federal audit-body documents (GAO) that report U.S. Coast Guard and U.S. Navy practice and relay Canadian, Norwegian and UK regulators; Japan and South Korea did not respond to GAO (GAO-24 p. 16). The flag still fires and the Anglo-American, U.S.-centred weighting increases. |
| Source Deception Risk | MSC/IMO primary documents: LOW for quoted text, MEDIUM for future roadmap projection. Status Book: LOW for reproduced status data, MEDIUM where official legal reliance requires depositary confirmation. SG/HET/BP: MEDIUM (author-owned; unaudited / partly untested). UKSC judgment: LOW for quoted text as recorded by the Round 3 audit (not re-checked in v0.4); MEDIUM for application to autonomous navigation (derived). GAO reports: LOW for GAO’s own findings as checked against the supplied PDFs in v0.5; MEDIUM for statements attributed to Coast Guard, Navy, IMO and stakeholder sources, which are second-hand; MEDIUM for applying Navy programme findings to commercial MASS (analogy). |
| Evidence rungs | [D-MSC/D-SB] normally Rung 4; [R] normally Rung 3 or 2; [S] Rung 2–0; [?] Rung 0; [D-UKSC] normally Rung 4 for quoted judgment text, as recorded by the Round 3 audit and not re-checked in v0.4. Proposed in v0.5: [D-GAO] Rung 4 for GAO’s own findings, Rung 3 for statements GAO attributes to officials or stakeholders (J6 item 12). |
| Mechanism-match Check | ANS is classified by mechanism as capacitive/contingent, not by vocabulary as “agent” in the legal sense. MASS 4.1 defines “Agent” to include software; SG agency faces still distinguish legal responsibility from software action. [D-MSC 4.1; R] |
| Supersession check | v0.5 supersedes v0.1, v0.2, v0.3, v0.4 and the amendment file as working draft. The MASS Code does not supersede SOLAS/COLREG/MARPOL; it supplements them. [D-MSC 1.2.1] |
| Isomorphic Cluster | Regulatory bridge / assurance translation systems: legacy obligation → new substrate → equivalence proof → certification. [R] |
| Fixed-point termination | The read terminates when no new core friction class appears in the supplied instruments. It does not claim no further flag-state or future-amendment frictions exist. [R] |
| Read target / Readability | System / Instance. Partially readable because operative texts and implementation practice are incomplete in the supplied sources. [R] |
| Reversibility | Regulatory interpretation is reversible by amendment, court decision, flag-state practice or IMO guidance; individual casualties are not reversible. [R] |

### B10. GAP MAP

Counts are declared claim-group counts, not a token census. v0.3 carried 34 : 18 : 14 (total 66) from v0.2 without an itemised group list, and its own note made a recount mandatory after fusion. v0.4 therefore recounts incrementally: it keeps the v0.3 baseline, moves one group, and adds the claim groups introduced by RT-01 to RT-10 and Insights A–D, itemised in the derivation table below. A from-scratch recount of every group remains an audit item. v0.1’s earlier map (47 : 12 : 6, total 65) and v0.3’s map (34 : 18 : 14, total 66) are superseded. v0.5 continues the incremental method: it keeps the v0.4 total, adds the claim groups introduced by the GAO fusion (second derivation table below), and leaves the from-scratch recount as an audit item. v0.4’s map (42 : 27 : 18, total 87) is superseded. [R]

| Category | Count | Basis |
| --- | --- | --- |
| Known [D] | 56 | Source-register claims, scope/status claims, directly quoted MASS provisions, Status Book amendment/final-clause facts, and UKSC holdings and paragraph quotations as recorded by the Round 3 audit ; v0.5 adds 14 GAO claim groups checked against the supplied PDFs (second derivation table) |
| Inferred [R] | 37 | Structural mappings, equivalence relations, transition-period effects, verification-stack analysis, and the v0.4 derived implications for ANS design, certification topology and approval-basis practice ; v0.5 adds 10 derived GAO-fusion groups |
| Unknown / external [S/?] | 24 | Operative rule text not supplied, flag-state practice, future mandatory regime, HET empirical validation, proposed design rules and thresholds, jurisdictional uptake of the UKSC test ; v0.5 adds 6 open groups |
| Total | 117 | Declared claim groups |
| Ratio | 56 : 37 : 24 | Known : inferred : open |

Recount derivation (v0.3 baseline to v0.4; retained as history):

| Step | Known [D] | Inferred [R] | Open [S/?] | Total | Groups |
| --- | --- | --- | --- | --- | --- |
| v0.3 baseline | 34 | 18 | 14 | 66 | As declared in v0.3 |
| Transfer | +1 | 0 | −1 | 0 | Ever Smart holding (the case-law group) moves from open to known on Round 3 verification (RT-01; GTL-08) |
| New [D] groups | +7 | 0 | 0 | +7 | UKSC paras 111–112; UKSC paras 60–61; UKSC para 40; COLREG Art. VI procedure; MASS 5.3.1 and 5.6.2; MASS 4.1 “Agent” definition; ABIL legal-basis provisions (Ch. 6, Annex 1 §1.4 and §2.5, Annex 2 §8.2, 5.1.3.4) |
| New [R] groups | 0 | +9 | 0 | +9 | Bearing-not-course ANS implication (#28); 17(a)(ii) observation versus 17(b) prediction split; decision-timing constraint on thresholds (#5); MASS 6.2 as framing principle; regulatory k_cap topology; agent/responsibility asymmetry; ABIL concept and mapping; mapping of UKSC groups to the S-5 states; practical COLREG freeze window |
| New open groups | 0 | 0 | +5 | +5 | S-5 design rule and numeric thresholds [S]; UKSC uptake outside the UK [?]; flag-state, class or IMO acceptance of S-5 [?]; ROC redundancy / k_cap limitation proposal [S]; whether the COLREG practical freeze holds to 2032 [?] |
| v0.4 total | 42 | 27 | 18 | 87 | Check: 34 + 1 + 7 = 42; 18 + 9 = 27; 14 − 1 + 5 = 18; 66 + 7 + 9 + 5 = 87 |

Operative COLREG rule text (Rules 2, 5–9, 15–17 and 19) is now cross-checked against UKSC- and HET-quoted text (GTL-06), but that group stays in the open count because the official consolidated text has not been checked. [R]

Recount derivation (v0.4 baseline to v0.5):

| Step | Known [D] | Inferred [R] | Open [S/?] | Total | Groups |
| --- | --- | --- | --- | --- | --- |
| v0.4 baseline | 42 | 27 | 18 | 87 | As declared in v0.4 |
| New [D] groups | +14 | 0 | 0 | +14 | (1) U.S. statutory minimum-crew and credential rules and the Coast Guard no-waiver position (GAO-24 pp. 2, 10, 12, fn. 21–23); (2) IMO look-out position and no-amendment position as reported (GAO-24 p. 13); (3) Pennsylvania Rule footnote and its stated causation factors (GAO-24 fn. 25); (4) IMO working-group agreements on master, ROC and multi-ship responsibility (GAO-24 p. 7); (5) IMO timeline as of May 2024 (GAO-24 p. 7); (6) Coast Guard case-by-case practice, equivalents, policy letters, AutoPoCo and rulemaking threshold (GAO-24 pp. 10–14, Table 1); (7) Canada, Norway and UK approaches (GAO-24 pp. 8–10, fn. 8–10); (8) stakeholder perspectives on safety, labour, cyber and physical security (GAO-24 pp. 5–6); (9) IMO degrees of autonomy (GAO-24 pp. 3–4, Fig. 2); (10) Navy operations-and-sustainment and digital-infrastructure cost omissions and the optimal-manning outcome (GAO-22 pp. 15–17, 23); (11) Navy shared digital infrastructure and autonomy architecture (GAO-22 pp. 3, 5, 23, 30); (12) Navy crew-to-software certification conversion and prototyping-plan gaps (GAO-22 pp. 31–34); (13) Navy prototype criteria, schedule and portfolio-governance findings (GAO-22 pp. 19–28); (14) Navy RAS siloed-approach, iterative-development and organization findings and later statutory changes (GAO-26 Snapshot; p. 2 fn. 5) |
| New [R] groups | 0 | +10 | 0 | +10 | (1) statutory minimum-crew friction as a bridge row and its ABIL implication (#29); (2) look-out equivalence evidence gap (G-17); (3) dual use of compliance evidence for liability disputes (#30); (4) version-lock versus iterative change tension (S-6, G-20); (5) precedent analogies S-7 and S-8; (6) commonality versus heterogeneity tension (F6); (7) master-level k_cap and one-ROC-at-a-time (F5 extension); (8) Administration plurality in practice (B3 addition); (9) remote-operation staffing and lifecycle cost basis unquantified (G-19); (10) corroboration of the practical COLREG freeze (A2 item 7 update) |
| New open groups | 0 | 0 | +6 | +6 | (1) post-August-2024 U.S. statute and policy developments [?]; (2) generalisation of U.S., Canadian, UK and Norwegian practice to other flag states [?]; (3) application of the Pennsylvania Rule to autonomous-vessel collisions [?]; (4) foreign regulators’ measures after 2024 [?]; (5) current relevance of 2022 Navy figures and 2025–2026 Navy reorganisation [?]; (6) whether legislative crew flexibility beyond the rocket-recovery pilot will be provided before 2032 [?] |
| v0.5 total | 56 | 37 | 24 | 117 | Check: 42 + 14 = 56; 27 + 10 = 37; 18 + 6 = 24; 87 + 14 + 10 + 6 = 117 |

The v0.5 recount is incremental, as in v0.4. A from-scratch recount of every group remains an audit item. [R]

## PART C — CROSS-REFERENCE MATRIX: FRICTION POINTS AND RESOLUTIONS

Each record has the same six fields: Legacy provision · MASS Code provision · Friction · Proposed resolution · Status · Tag. IDs #1–#30 and S-1–S-8 are stable; #1–#27 and S-1–S-4 match the numbering used in v0.1, v0.2 and v0.3, #28 and S-5 were added at v0.4 (Round 3), and #29, #30 and S-6 to S-8 were added at v0.5 (GAO fusion). Status values carry v0.1’s resolution labels, reconciled to v0.2’s corrections and the Round 3 audit. [R]

### C0. INDEX

| ID | Topic | Legacy instrument | Status |
| --- | --- | --- | --- |
| #1 | Look-out “sight and hearing” (Rule 5) | COLREG | Resolved in principle; equivalence to be shown |
| #2 | Responsibility / immediate danger, remote master (Rule 2) | COLREG | Partially resolved; latency undefined |
| #3 | Safe speed vs OE (Rule 6) | COLREG | Partially resolved; cliff problem |
| #4 | “Scanty information” (Rule 7) | COLREG | Unresolved |
| #5 | Readily apparent action (Rule 8) | COLREG | Partially resolved |
| #6 | Narrow channels / TSS; small MASS (Rules 9–10) | COLREG | Unresolved for small MASS |
| #7 | Stand-on action threshold (Rule 17(a)(ii)) | COLREG | Unresolved |
| #8 | Stand-on prediction (Rule 17(b)) | COLREG | Unresolved |
| #9 | Restricted visibility (Rule 19) | COLREG | Partially resolved |
| #10 | Lights, shapes, sound signals (Parts C/D) | COLREG | Unresolved at verification level |
| #11 | Limitations of vessel and crew (Rule 2) | COLREG | Resolved by substitution |
| #12 | Verification of compliance (Part F) | COLREG | Layered; both levels required |
| #13 | Navigational equipment, VDR (V/19, V/20) | SOLAS | Partially resolved |
| #14 | Stability, watertight integrity (II-1) | SOLAS | Resolved by automation |
| #15 | Fire protection (II-2) | SOLAS | Resolved by automation and remote control |
| #16 | Life-saving appliances; distress assistance (III, V/33) | SOLAS | Resolved by modification |
| #17 | Maritime security / ISPS (XI-2) | SOLAS / ISPS | Resolved by extension |
| #18 | Safety management (IX) | ISM | Resolved by alternative certification |
| #19 | Training, watchkeeping, sea service | STCW | Partially resolved |
| #20 | Oil pollution / IOPP (Annex I) | MARPOL | Unresolved |
| #21 | Sewage (Annex IV) | MARPOL | Conditionally applicable |
| #22 | Garbage (Annex V) | MARPOL | Conditionally applicable |
| #23 | Air pollution (Annex VI) | MARPOL | Unresolved |
| #24 | Incident reports (Protocol I) | MARPOL | Partially resolved |
| #25 | Rule 9 vs Rules 15–17 interaction | COLREG / case law | Verified; jurisdiction-specific (UKSC); operationalizable as ANS design threshold |
| #26 | Navigation-responsibility split | SOLAS / COLREG / ISM | Unresolved at IMO level; mitigable by ConOps matrix |
| #27 | Verification stack | SOLAS / COLREG / III Code | Layered; keep distinct |
| #28 | No steady course requirement | COLREG Rules 7, 15 | Unresolved — requires ANS design change |
| #29 | Statutory minimum crew and human-presence presumptions | Flag-state statute (U.S. Title 46 as reported) / MASS Code | Unresolved — statutory; U.S. data point |
| #30 | Liability presumption for COLREG non-compliance (Pennsylvania Rule) | U.S. admiralty case law / COLREG | Open — outside instrument scope; counsel needed |
| S-1 | Load Lines / IS Code | Load Lines | Open |
| S-2 | MARPOL e-records; unmanned-barge precedent | MARPOL | Analogy only |
| S-3 | 2023–2026 amendment-version drift | SOLAS / MARPOL | Open |
| S-4 | MASS Code application gate | MASS Code | Open |
| S-5 | Rule-switching trigger at channel entrances | COLREG / UKSC | Unresolved — proposed design rule |
| S-6 | Version-locked approval basis vs iterative software change | MASS Code | Open — derived tension |
| S-7 | Crew-executed certifications converted to software-executed | Navy certification practice | Analogy only |
| S-8 | U.S. automated-vessel crew-substitution precedent (46 CFR) | USCG regulations | Analogy only |

### C1. COLREG ↔ MASS CODE

#### #1 · Look-out by sight and hearing (Rule 5)

- Legacy: COLREG Rule 5 — “proper look-out by sight and hearing as well as by all available means.”
- MASS Code: 16.4.2 (ANS “should maintain adequate situational awareness”; EP1 continuous monitoring of information necessary for safe navigation, based on the OE); 4.33 (situational awareness = perception, comprehension, projection).
- Friction: “Sight and hearing” are human sensory modalities; the ANS uses sensor fusion (radar, EO/IR, AIS, LIDAR, acoustic). The Rule 5 text does not name sensors and is unchanged.
- Resolution: Treat “situational awareness” as a functional-equivalence candidate. Working mapping: sensor fusion ↔ sight; acoustic sensing ↔ hearing; data link ↔ “all available means” [R]. Declare sensor suite, degradation modes and lookout-equivalence in ConOps and V&V, and demonstrate equivalence in the regulatory gap analysis [D-MSC Annex 2 §8.2]. Do not claim the COLREG text changed.
- Status: Resolved in principle; equivalence must be demonstrated per vessel.
- Tag: [D-HET §6.3]; [D-MSC 16.4.2, 4.33, Annex 2 §8.2]; [R]
- GAO fusion (v0.5, GF-02, GF-08): GAO-24 (p. 13) reports Coast Guard officials saying that IMO determined autonomous ships must still meet the look-out requirement without amending the international regulation, and that the Coast Guard has seen no examples of autonomous look-out technology to evaluate because stakeholders have not provided any, so how such technology complies with collision regulations is not yet established for U.S. purposes. This confirms that the Rule 5 equivalence demonstration above is the Submitter’s burden and that no accepted reference test exists in that flag state (G-17, GTL-18). A shipbuilder also raised the camera limitation for small, hard-to-see people near a ship, such as a kayaker in a harbour (GAO-24 p. 5). [D-GAO24 pp. 5, 13; R; ?]

#### #2 · Responsibility and departure to avoid immediate danger (Rule 2)

- Legacy: COLREG Rule 2 — responsibility of vessel, owner, master and crew; departure from the Rules to avoid immediate danger.
- MASS Code: 8.7.1–8.7.4; 14.2.1.10–.14 (master responsible for safe operation at all times; may be on board or at a ROC).
- Friction: Rule 2 assumes a master on the bridge. For a MASS the master may be at a ROC, so the “immediate danger” judgment is made remotely, with latency.
- Resolution: Master responsibility persists regardless of location. Rule 2 departure authority transfers to the remote master, but the ANS needs a pre-programmed fallback response for the interval between danger detection and master intervention [D-MSC 8.4.2]. Declare maximum intervention latency, fallback response and authority transfer in the ConOps. If persons are on board, the master must be on board [D-MSC 14.2.1.12]. The Code specifies no maximum latency (see G-3).
- Status: Partially resolved; latency undefined.
- Tag: [D-HET Rule 2 excerpt]; [D-MSC]; [R]

#### #3 · Safe speed (Rule 6)

- Legacy: COLREG Rule 6 — safe speed at all times, weighing visibility, traffic density, manoeuvrability, background lights, wind/sea/current, draught and radar characteristics.
- MASS Code: 8.3.1 (OE contains a “description of the environmental limitations”); 16.3.2 (ANS maintains functionality under expected OE conditions); 8.3.3, 8.4.
- Friction: Rule 6 is a continuous human judgment; the OE is a discrete boundary. The transition from inside to outside the OE is a cliff, not a gradient.
- Resolution: Convert Rule 6 factors into OE parameters: safe speed = the speed at which the MASS remains within its OE; exceeding OE limits drives degraded state or fallback [D-MSC 8.3.3, 8.4]. Encode factors as OE limits with monitored margins and define degraded-state buffers before OE exit, to avoid cliff-only logic.
- Status: Partially resolved; cliff problem open.
- Tag: [D-HET Rule 6 excerpt]; [D-MSC 8.3, 8.4, 16.3.2]; [R]

#### #4 · Assumptions on scanty information (Rule 7)

- Legacy: COLREG Rule 7 — no assumptions on the basis of scanty information, especially scanty radar information.
- MASS Code: 16.4.2 EP2 (continuous analysis, projecting future statuses); 16.4.3 EP2 (avoidance action based on risk assessment); 13.4.1.4 (alert to master).
- Friction: The ANS may act on incomplete sensor data (degradation, weather interference). “Scanty” has no sensor-data threshold in the Code.
- Resolution: Define a sensor sufficiency threshold and uncertainty floor analogous to Rule 7; below it the ANS alerts the master and enters degraded/fallback state as risk-assessed. Declare it in the OE/ODD. This is a gap in the Code; whether IMO will adopt a threshold is [?].
- Status: Unresolved.
- Tag: [D-HET Rule 7 excerpt]; [D-MSC 16.4.2 EP2, 16.4.3 EP2, 13.4.1.4]; [R]; [?]

#### #5 · Action must be readily apparent (Rule 8)

- Legacy: COLREG Rule 8 — action to avoid collision positive, in ample time, and large enough to be readily apparent to another vessel observing visually or by radar.
- MASS Code: 16.4.3 EP1–EP3 (means to act in accordance with COLREG; decisions timely and within safe operating limits).
- Friction: The other vessel may be conventional (human lookout) or another MASS (sensor-based); small incremental manoeuvres may be unreadable. The Code does not say how ANS actions are made “readily apparent” and does not address Part D sound signals for unmanned vessels. The UKSC (para 40, quoting Sheen J in The Maloja II) adds a temporal constraint: “Manoeuvres taken to avoid a close-quarters situation should be taken at a time when the responsible officer does not have to make a quick decision or a decision based on inadequate information. Those manoeuvres should be such as to be readily apparent to the other ship.” [D-UKSC para 40] This constrains the CPA/TCPA threshold: if the ANS waits too long, any manoeuvre will fail the “readily apparent” test because it will be made under time pressure. The threshold must be set early enough to allow a “positive” action “made in ample time” (Rule 8(a)). [D-UKSC para 40; R]
- Resolution: Validate manoeuvre legibility to (a) human visual/radar observers and (b) other MASS sensors. Digital signalling (AIS, VDES) may supplement for MASS-to-MASS encounters [R]. Include sound/light signal compliance where applicable; Part D signals are physical appliances (whistle, bell, gong) [S/GTL]. The “readily apparent” test is not just about manoeuvre magnitude but about decision timing. The ANS must decide early enough that: (1) the decision is not made under time pressure; (2) the decision is not made on inadequate information; (3) the resulting manoeuvre is large enough to be readily apparent. Declare maximum decision latency in the ConOps. [D-UKSC para 40; D-MSC 16.4.3 EP1; R]
- Status: Partially resolved.
- Tag: [D-HET Rule 8 excerpt]; [D-MSC 16.2, 16.4.3]; [S/GTL Part D]; [R]; [D-UKSC para 40]
- GAO fusion (v0.5, GF-07): Canada’s 2022 policy for small autonomous ships (12 m or less, or 15 gross tons or less) requires a device broadcasting a distinct signal that identifies the ship as autonomous, and prior notice of operations to the local Canadian Coast Guard (GAO-24 p. 8, fn. 8). This is a flag-state example of announcing autonomy to other vessels, which this row had only proposed as an AIS/VDES supplement [R]. It is a small-ship policy, not a rule for MASS Code ships. [D-GAO24 p. 8, fn. 8; R]
- Verification note (v0.5.2, VR-11): the excerpts of Canada’s small-MASS policy read in round 1b did not show the distinct-signal and prior-notice requirements that GAO-24 reports. Do not rely on that point until the policy text and annexes are read. [D-TC; ?]

#### #6 · Narrow channels and traffic separation; small MASS (Rules 9–10)

- Legacy: COLREG Rule 9 (narrow channels); Rule 10 (traffic separation schemes), including 10(j): a vessel under 20 m or a sailing vessel shall not impede a power-driven vessel following a traffic lane [S/GTL].
- MASS Code: 16.4.4 (ANS executes the voyage plan; EP1 route within allowable deviation); 2.1; Res. §3.
- Friction: Rules 9–10 require specific behaviour in constrained waters, which the voyage plan must encode. Small MASS (below 500 GT, possibly below 20 m) are only invited to apply the Code yet remain subject to COLREG; a small MASS entering a TSS is bound by Rule 10 but may not be covered by the Code.
- Resolution: Flag states should define small-MASS rules; the ConOps must declare TSS/narrow-channel behaviour and the rule set applied. No IMO-level resolution exists.
- Status: Unresolved for small MASS. Flag-state practice is [?] (GTL-15).
- Tag: [S/GTL COLREG operative text]; [D-MSC 2.1, 16.4.4, Res. §3]; [R]
- GAO fusion (v0.5, GF-07): flag-state small-craft practice now has partial evidence: Canada’s Tier I small-autonomous-ship policy (12 m / 15 GT) and, for the UK, December 2023 changes allowing remote operation of vessels under 24 m with new definitions and some exemptions (GAO-24 pp. 8–9, fn. 8, 10). Both are national small-vessel measures reported in 2024. GTL-15 stays open for other flag states and for current versions (GTL-21). [D-GAO24 pp. 8–9; ?]
- Verification update (v0.5.2, VR-11, VR-12): Canada’s Tier I Policy TP 13585 (effective 1 February 2022) is confirmed in excerpts: it applies to small MASS of degree three or four (no crew or passengers aboard) of 12 m or less in length or 15 gross tons or less, routes applications for alternative safety requirements to the Marine Technical Review Board, and exempts very small craft (2 m or less, 100 kg or less) under conditions; a separate Tier I policy on autonomous navigation systems aboard vessels also exists and was not read. UK SI 2023/1216 came into force on 13 December 2023; it defines a remotely operated unmanned vessel as a small vessel (under 24 m load-line length) operated from a remote operation centre and carrying no person, and requires the log book to be kept at the remote operation centre. [D-TC; D-UKSI; ?]

#### #7 · Stand-on action threshold (Rule 17(a)(ii))

- Legacy: COLREG Rule 17(a)(ii) — the stand-on vessel may act by her manoeuvre alone as soon as it becomes apparent that the give-way vessel is not taking appropriate action.
- MASS Code: 16.4.3; 8.7.1 (ability to “intervene and/or override the system”); 16.5.
- Friction: “Becomes apparent” is a human perceptual judgment. For an ANS it must become a sensor-fusion/prediction threshold: at what CPA/TCPA does the ANS conclude the give-way vessel is not acting? The UKSC confirms (paras 60–61) that Rule 17(a)(ii) is a permissive threshold with an observation-based trigger (“becomes apparent”). The ANS must implement a change-detection algorithm on the give-way vessel’s behaviour: is she taking appropriate action? This is an OBSERVATION problem. The trigger is: the give-way vessel’s observed actions deviate from expected COLREG-compliant behaviour beyond a declared threshold. [D-UKSC paras 60–61; D-HET §6.3; R]
- Resolution: Declare a CPA/TCPA or equivalent risk threshold at which the ANS moves from monitoring to executing a stand-on avoidance manoeuvre, in the ConOps [D-MSC 8.2]; validate it in approval [D-MSC Annex 1] and against encounter scenarios; permit override per 16.5. Different ANS implementations will set different thresholds — a genuine DOF [D-HET §6.3] that must be bounded. Distinguish explicitly in the ConOps: 17(a)(ii) threshold = observation-based change detection; 17(b) threshold = prediction-based trajectory modelling. These are different algorithms with different accuracy requirements. Declare both in the approval basis. [D-MSC Annex 1; R]
- Status: Unresolved (threshold undefined).
- Tag: [D-HET Rule 17 excerpt]; [D-MSC]; [R]; [D-UKSC paras 60–61]

#### #8 · Stand-on prediction (Rule 17(b))

- Legacy: COLREG Rule 17(b) — the stand-on vessel takes the action that best aids avoidance when collision cannot be avoided by the give-way vessel alone.
- MASS Code: 4.33 (situational awareness includes projection of future status); 16.4.2 EP2; Annex 1 §2.7.
- Friction: “Cannot be avoided” is an inference about another agent’s future behaviour — a prediction problem, and arguably the hardest COLREG rule for an ANS [R]. The Code requires projection but sets no prediction-accuracy requirement. The UKSC confirms (paras 60–61) that Rule 17(b) is a mandatory threshold with a prediction-based trigger (“collision cannot be avoided by the action of the give-way vessel alone”). The ANS must implement a predictive algorithm on the give-way vessel’s trajectory: can she avoid collision alone? This is a PREDICTION problem, distinct from the observation problem of 17(a)(ii). The trigger requires the ANS to model the give-way vessel’s manoeuvring capability and predict whether her solo action is sufficient. Prediction-accuracy requirements are stricter than observation thresholds. [D-UKSC paras 60–61; D-HET §6.3; R]
- Resolution: The V&V plan must include prediction uncertainty, false-negative / false-positive thresholds and escalation criteria. If prediction accuracy falls below the declared threshold, the ANS escalates to the human master [D-MSC Annex 1 §2.7; R]. Prediction-accuracy standards are [?].
- Status: Unresolved.
- Tag: [D-HET Rule 17 excerpt]; [D-MSC]; [R]; [?]; [D-UKSC paras 60–61]

#### #9 · Restricted visibility (Rule 19)

- Legacy: COLREG Rule 19 — safe speed adapted to circumstances; a vessel that detects another by radar alone must determine whether a close-quarters situation is developing. Specific obligations include speed reduction and avoiding certain course alterations (e.g., to port for a vessel forward of the beam) [S/GTL].
- MASS Code: 16.4.2–16.4.3; 8.3.1.2.3.
- Friction: Rule 19 assumes radar as the primary sensor; a MASS may fuse EO/IR, LIDAR, acoustic and radar, so “detects by radar alone” does not map. The Code’s situational awareness is sensor-agnostic but does not encode Rule 19’s specific obligations.
- Resolution: Declare restricted-visibility mode, sensor assumptions, speed policy and prohibited manoeuvres in the ConOps. Define equivalent sensor-fusion states for “restricted visibility” and “detected by radar alone.” The OE [8.3.1.2.3] already covers visibility limits.
- Status: Partially resolved.
- Tag: [D-HET Rule 19 excerpt]; [D-MSC 8.3.1.2.3, 16.4.2–16.4.3]; [S/GTL]; [R]

#### #10 · Lights, shapes, sound and light signals (Parts C/D, Rules 20–37)

- Legacy: COLREG Rules 20–31 (lights and shapes); Rules 32–37 (sound and light signals).
- MASS Code: 16.2; Part III has no dedicated lights/shapes/sound-signal chapter; 5.1.1 and 5.1.5 (MASS Safety Certificate and MASS Record issued in addition to SOLAS I/12 certificates).
- Friction: COLREG applies to MASS unchanged, but the Code does not say who or what activates sound signals (Rule 35) with no crew, or how Parts C/D are verified for unmanned vessels in surveys. The gap is verification and implementation, not applicability (see BR-03).
- Resolution: Add an explicit survey/V&V checklist for lights, shapes, automated sound signals, failure modes and manual/remote override. The Code should state that Parts C/D apply or provide equivalent arrangements.
- Status: Unresolved at verification level.
- Tag: [S/GTL COLREG operative details]; [D-MSC 16.2, 5.1.1, 5.1.5, Part III contents]; [R]; [?] Code silence
- GAO fusion (v0.5, GF-07): Canada’s small-ship policy requires a distinct broadcast signal identifying an autonomous ship (see #5). No flag-state measure reported by GAO addresses who or what activates Rule 35 sound signals on a crewless ship. [D-GAO24 p. 8; ?]
- Verification note (v0.5.2, VR-12): a law-firm summary of the UK Workboat Code Edition 3 Annex 2 says a remotely operated unmanned vessel that loses connectivity must show or sound not-under-command signals. That would put signal activation on the vessel itself on loss of link, a partial answer to the open question above for small UK workboats only. Annex 2 text not read. [secondary; ?]

#### #11 · Limitations of the vessel and her crew (Rule 2)

- Legacy: COLREG Rule 2 — due regard to special circumstances, including “the limitations of herself and her crew.”
- MASS Code: 8.7.2 (crew and remote operators always able and prepared to take over autonomous functions without risk to the outcome of the task); 14.2.1.
- Friction: With no crew on board the crew-limitation clause is vacuous on its face; the Code replaces it with human oversight capability [8.7].
- Resolution: Substitution: declare a human-system limitation analysis covering remote operators and the system; do not treat absence of crew as absence of limitations. Document the substitution in the regulatory gap analysis [D-MSC Annex 2 §8.2].
- Status: Resolved by substitution.
- Tag: [D-HET Rule 2 excerpt]; [D-MSC 8.7.2, 14.2.1, Annex 2 §8.2]; [R]

#### #12 · Verification of compliance (Part F, Rules 39–41)

- Legacy: COLREG Part F — verification of compliance through the IMO Member State Audit Scheme.
- MASS Code: Ch. 5.1–5.9 (surveys and certificates); 6.1 (approval process).
- Friction: COLREG verification operates at flag-state level; the Code verifies at vessel/ROC level. The granularity differs.
- Resolution: Build an evidence stack: flag-state implementation audit + MASS/ROC certificates + vessel incident data. Both levels are needed; neither substitutes for the other.
- Status: Layered; both required.
- Tag: [D-HET Part F excerpt]; [D-MSC 5–6]; [R]; [GTL]

### C2. SOLAS / ISM / ISPS / STCW ↔ MASS CODE

#### #13 · Navigational equipment and VDR (SOLAS V/19, V/20)

- Legacy: SOLAS Ch. V Reg. 19 (carriage requirements for shipborne navigational systems: radar, ECDIS, AIS, VDR, etc.); Reg. 20 (voyage data recorders).
- MASS Code: 16.3.3 EP1 (V/19.2.1.4 and .5 met “by electronic means”); 9.10.6 (V/20 applies to all MASS).
- Friction: V/19 assumes a human navigator operating equipment on a bridge. A MASS has no bridge or an unmanned one, so equipment must be remotely accessible and machine-readable.
- Resolution: Electronic means = the ANS reads ECDIS data directly; back-up = redundant electronic chart system [R]. Resolved in principle, not in detail. Verify operative SOLAS text externally.
- Status: Partially resolved.
- Tag: [D-MSC 16.3.3 EP1, 9.10.6]; [S/GTL SOLAS text]; [R]

#### #14 · Structure, subdivision, stability, watertight integrity (SOLAS II-1)

- Legacy: SOLAS Ch. II-1.
- MASS Code: Ch. 19; 19.2.2 (SCS continuously assesses intact stability and supports survivability assessment in case of damage).
- Friction: Stability criteria assume crew corrective action (ballast transfer, damage control); a MASS may have no crew for it.
- Resolution: The SCS provides the monitoring and alerting function that crew would; II-1 criteria still apply. Declare the human/remote response chain.
- Status: Resolved by automation.
- Tag: [D-MSC 19.2.2]; [S/GTL SOLAS text]; [R]

#### #15 · Fire protection, detection, extinction (SOLAS II-2)

- Legacy: SOLAS Ch. II-2.
- MASS Code: Ch. 20; 20.2.4–20.2.8 (20.2.7: remote and onboard control of all active fire protection measures; 20.2.8: facilitate intervention from external fire responders).
- Friction: Firefighting traditionally assumes crew; a MASS has none.
- Resolution: II-2 objectives apply. Crew firefighting is replaced by automated detection + remote/autonomous extinction + an external-responder interface. Validate single-compartment fire control and fallback logic.
- Status: Resolved by automation and remote control.
- Tag: [D-MSC 20.2.7–20.2.8]; [R]

#### #16 · Life-saving appliances; distress assistance (SOLAS III, V/33)

- Legacy: SOLAS Ch. III (LSA); Ch. V Reg. 33 (assistance to persons in distress).
- MASS Code: Ch. 21; 21.2.1–21.2.4 (21.2.3: rescue equipment usable independently of crew; 21.2.4: retrieved persons safely accommodated).
- Friction: Ch. III assumes crew; a MASS may have none but must still assist persons in distress.
- Resolution: Modification: rescue equipment deployable without crew; accommodation for rescued persons; retrieved persons able to communicate with the ROC.
- Status: Resolved by modification.
- Tag: [D-MSC 21.2.1–21.2.4]; [S/GTL SOLAS V/33]; [R]

#### #17 · Maritime security (SOLAS XI-2 / ISPS Code)

- Legacy: SOLAS Ch. XI-2 and the ISPS Code (physical ship security: access control, restricted areas, onboard security officers).
- MASS Code: Ch. 12; 12.4 (12.4.1: SSP accounts for ROC; 12.4.2.2: remote operators take part in ISPS training, drills and exercises; 12.4.3: ROC security breach triggers fallback).
- Friction: The ROC becomes a new security target and a MASS has no onboard security officer.
- Resolution: Extension: the SSP must account for the ROC; remote operators participate in ISPS training/drills; ROC compromise triggers isolation/fallback. Remote operators inherit transferred security responsibilities — do not claim the remote operator automatically replaces the SSO (see C-14).
- Status: Resolved by extension.
- Tag: [D-MSC 12.2, 12.4.1–12.4.3]; [R]
- GAO fusion (v0.5, GF-08): many stakeholders told GAO that higher autonomy raises theft and vandalism risk because no human aboard deters intruders, while some said remote operators could do camera-based security rounds and issue audible warnings (GAO-24 p. 6). Stakeholder opinion, not tested evidence; it supports declaring ROC security duties as transferred responsibilities, not as an automatic SSO replacement. [D-GAO24 p. 6; R]

#### #18 · Safety management (ISM Code / SOLAS IX)

- Legacy: ISM Code — Company → Master → Crew; Document of Compliance and Safety Management Certificate.
- MASS Code: Ch. 11; 5.7; 11.2–11.3 (ROCSMS, ROM DoC, RMC).
- Friction: The ROC is a further node and the DoC/SMC do not account for it.
- Resolution: Use the SMS plus ROCSMS / ROM DoC / RMC where alternative ROC management is approved; define responsibility interfaces. The triangle becomes a quadrilateral: Company ↔ MASS ↔ ROC ↔ Master [R].
- Status: Resolved by alternative certification.
- Tag: [D-MSC 5.7, 11.2–11.3]; [R]

#### #19 · Training, watchkeeping, sea service (STCW)

- Legacy: STCW Convention and Code (sea-going service, onboard watchkeeping; A-VIII/1 hours of rest).
- MASS Code: Ch. 14; 14.1.3 (ROC may be considered a directly associated location to the navigational bridge); 14.2.1.8–.9 (fatigue/rest principles); 14.2.2.1 (remote operators qualified to a level not less than STCW 1978); 14.2.2.3; 14.5.1 (remote operational experience may be considered equivalent to approved sea-going service).
- Friction: Remote operators are not onboard watchkeepers; STCW sea-service assumptions do not map directly.
- Resolution: STCW-level qualification applies; the sea-service requirement is replaceable by remote operational experience at the Administration’s discretion. Fatigue/rest principles already apply; the open item is ROC-specific implementation (hours/rest quantification, see G-7 and GTL-10).
- Status: Partially resolved.
- Tag: [D-MSC 14.1.3, 14.2.1.8–.9, 14.2.2, 14.5.1]; [S/GTL STCW]; [R]
- GAO fusion (v0.5, GF-07, GF-08): (a) IMO’s regulatory scoping identified as priority issues the roles of master and crew, the roles of people who operate ships remotely, and designating remote operators as seafarers (GAO-24 p. 7), which bears on whether STCW sea-service and qualification rules reach remote operators. (b) Norway let the minimum crew of Yara Birkeland fall from five to three after successful tests with no safety incident, with the owner hoping for two (GAO-24 p. 9): an example of incremental, test-based crew reduction by a regulator. (c) Stakeholders cited union opposition and retraining needs (GAO-24 p. 6). [D-GAO24 pp. 6, 7, 9; R]

### C3. MARPOL ↔ MASS CODE

#### #20 · Oil pollution prevention; IOPP (MARPOL Annex I)

- Legacy: MARPOL Annex I — oil discharge monitoring, oily water separators, IOPP Certificate and surveys.
- MASS Code: 9.10; Ch. 24; no Annex-I-specific provision.
- Friction: MASS machinery spaces may be unmanned, so monitoring must be automated. The Code does not address Annex I compliance, though a MASS is still a ship under MARPOL (the Code is “supplementary to other IMO instruments such as SOLAS,” Preamble 5, which implies MARPOL applies [R]).
- Resolution: Annex I applies unchanged. Add a MARPOL Annex I compliance checklist to the ConOps / MASS Record; automate oil-discharge monitoring and logging; verify how IOPP surveys treat unmanned machinery spaces.
- Status: Unresolved; Code gap.
- Tag: [D-MSC Part III contents, 9.10, 24, Preamble 5]; [S/GTL MARPOL Annex I]; [R]

#### #21 · Sewage (MARPOL Annex IV)

- Legacy: MARPOL Annex IV.
- MASS Code: 21.2.4; 2.3 (modes with persons on board).
- Friction: “No crew” does not mean no persons ever: maintenance crews, pilots, rescued persons or mixed modes of operation can generate sewage. (Corrects v0.1’s “trivially resolved.”)
- Resolution: Apply Annex IV whenever applicable persons or source streams exist; declare zero-person operating periods and reception/holding arrangements.
- Status: Conditionally applicable.
- Tag: [D-MSC 21.2.4, 2.3]; [S/GTL MARPOL Annex IV]; [R]

#### #22 · Garbage (MARPOL Annex V)

- Legacy: MARPOL Annex V.
- MASS Code: Ch. 22; 9.10; Ch. 24.
- Friction: Garbage can arise from cargo residues, packaging, maintenance, stores, equipment, lost items and persons even without a permanent crew. (Corrects v0.1’s “no crew = no garbage.”)
- Resolution: Add a garbage-management plan by voyage phase and person-presence mode.
- Status: Conditionally applicable.
- Tag: [D-MSC 22, 9.10]; [S/GTL MARPOL Annex V]; [R]

#### #23 · Air pollution: NOx, SOx, GHG (MARPOL Annex VI)

- Legacy: MARPOL Annex VI.
- MASS Code: Ch. 24; 24.2.3–24.2.9 (24.2.3: machinery sufficient for autonomous and remotely operated functions to be maintained).
- Friction: The machinery chapter addresses safe and reliable machinery, not emissions compliance. A MASS may use alternative propulsion (electric, hybrid, wind-assist).
- Resolution: Annex VI compliance remains separate; alternative propulsion must satisfy applicable emissions and fuel rules or approved equivalents.
- Status: Unresolved.
- Tag: [D-MSC 24.2.3–24.2.9]; [S/GTL MARPOL Annex VI]; [R]

#### #24 · Incident reports (MARPOL Protocol I)

- Legacy: MARPOL Protocol I — reports on incidents involving harmful substances.
- MASS Code: 9.10.5 (logged data available to the Administration and investigation authorities on request); Ch. 17–18 (communications).
- Friction: Incident reporting needs a responsible actor and communications; data availability is not the same as an immediate report. Who reports — the ANS, the remote operator or the master?
- Resolution: Assign the reporting duty to master / Company / ROC in the ConOps and SMS; automate detection and log support; verify communications availability.
- Status: Partially resolved.
- Tag: [D-MSC 9.10.5, 17, 18]; [S/GTL MARPOL Protocol I]; [R]

### C4. INTER-INSTRUMENT, CASE-LAW AND NATIONAL-LAW FRICTION (#25–#30)

#### #25 · Rule 9 (narrow channel) vs Rules 15–17 (crossing)

- Instruments: COLREG; UKSC [2021] UKSC 6 (case law).
- Evidence: Evergreen Marine (UK) Ltd v Nautical Challenge Ltd [2021] UKSC 6 (the “Ever Smart” case). The UKSC held (para 145): “Where an outbound vessel in a narrow channel is crossing with an approaching vessel so as to involve a risk of collision, the crossing rules are NOT overridden by the narrow channel rules merely because the approaching vessel is intending and preparing to enter the narrow channel. The crossing rules are ONLY overridden if and when the approaching vessel is shaping to enter, adjusting her course so as to reach the entrance on her starboard side of it, on her final approach.” [D-UKSC para 145]
- Friction: The COLREG text is unchanged; the interaction was settled by one court, not by IMO amendment. The ANS’s collision-avoidance logic must encode some interpretation.
- Three-phase test established by the UKSC [D-UKSC paras 134–145]:
  - Group 1 — vessel crossing the entrance but NOT intending to enter → crossing rules apply.
  - Group 2 — vessel shaping to enter on final approach → narrow channel rules override.
  - Group 3 — vessel intending or preparing to enter but NOT YET shaping (for example, waiting for a pilot) → crossing rules STILL apply.
  - ALEXANDRA 1 was in Group 3 (waiting for a pilot), and the UKSC held the crossing rules applied to her. This is a scenario a MASS can face: a vessel waiting outside a channel entrance while the MASS exits. [D-UKSC paras 134–145; R]
- Resolution: Treat the holding as a jurisdiction-specific interpretation (UK law; persuasive elsewhere). The ConOps must declare the flag/coastal-state interpretation and the collision-avoidance rule priority and, where the jurisdiction recognizes the UKSC test, encode it as the rule-switching logic in S-5 (K4). The encoded choice is a genuine DOF [D-HET §6.3] bounded by the ConOps. [D-UKSC; R]
- Status: Verified; jurisdiction-specific (UKSC); operationalizable as ANS design threshold.
- Tag: [D-UKSC para 145; R]
- GAO fusion (v0.5, GF-02): GAO-24 does not mention the UKSC judgment and was written before the MASS Code. It reports (p. 13) that, as of mid-2024, how autonomous technology complies with collision regulations was not yet established for the Coast Guard, and that each country must decide how to meet the look-out requirement. This supports the jurisdiction-declaration requirement above without adding evidence on the Rule 9 / Rules 15–17 interaction. [D-GAO24 p. 13; R]

#### #26 · Navigation-responsibility split

- Instruments: SOLAS, COLREG, ISM, MASS Code.
- Evidence: Three legacy instruments assign navigation-safety responsibility to three entities: master (COLREG Rule 2), company (ISM) and flag state (SOLAS). The Code preserves the human master, Company SMS, ROC management and Administration approval; the ANS acts as a system. [D-MSC 8.6.2, 8.7, 11, 14, Annex 1 §2.4]
- Friction: The master may be at a ROC, the company operates the ROC, and the flag state certifies both.
- Working responsibility chain: Flag State → Company → ROC → Master → ANS, each link governed by a different instrument. [R]
- Resolution: Create a responsibility-allocation matrix in the ConOps and task allocation summary. The approval basis [D-MSC Ch. 6] must verify there is no responsibility gap; the regulatory gap analysis [D-MSC Annex 2 §8.2] should document how responsibility flows from flag state to ANS.
- Status: Unresolved at IMO level; mitigable by ConOps matrix.
- Tag: [D-MSC 8.6.2, 8.7, 11, 14, Annex 1 §2.4, Ch. 6]; [R]
- GAO fusion (v0.5, GF-04, GF-14): the IMO working-group positions on masters and remote operating centres (B3 addition) fit the responsibility chain above. GAO-22 (pp. 21–22) found that the Navy had no empowered leader for its whole uncrewed effort, and GAO-26 (Snapshot) found inconsistent leadership and unformalized stakeholder roles still creating inefficiency. These are military-programme findings used as analogy only: a chain with a gap at the integrating role is a documented failure pattern, so the no-responsibility-gap check in the approval basis is worth keeping. [D-GAO22 pp. 21–22; D-GAO26 Snapshot; R]

#### #27 · Verification stack

- Instruments: SOLAS XI-1/6; COLREG Part F; III Code; MASS Code Ch. 5–6.
- Evidence: SOLAS XI-1/6 requires casualty investigation. COLREG Part F provides flag-state audit. The III Code became mandatory through SOLAS Ch. XIII on 1 January 2016 [D-SB SOLAS entry (130)]. MASS Ch. 5–6 adds a vessel/ROC survey and approval layer.
- Friction: Four overlapping verification regimes with different granularity.
- Resolution: Keep the layers distinct and do not collapse them into one audit: (1) III Code — flag-state implementation; (2) COLREG Part F — COLREG-specific compliance; (3) SOLAS XI-1/6 — casualty investigation; (4) MASS Ch. 5–6 — vessel/ROC certificates and approval. No strict hierarchy among them is asserted.
- Status: Layered; keep distinct.
- Tag: [D-SB SOLAS entry (130)]; [D-MSC 5–6]; [D-HET Part F]; [R]

#### #28 · No steady course requirement for crossing rules (added v0.4, RT-02)

- Legacy: COLREG Rules 7(d)(i) and 15. Rule 7(d)(i): “such risk shall be deemed to exist if the compass bearing of an approaching vessel does not appreciably change.” Rule 15: “When two power-driven vessels are crossing so as to involve risk of collision, the vessel which has the other on her own starboard side shall keep out of the way.” [D-UKSC para 45]
- MASS Code: 16.4.2 (situational awareness); 16.4.3 (collision avoidance); Annex 1 §2.7 (V&V plan). [D-MSC]
- Friction: The UKSC held (para 111): “if two vessels, both moving over the ground, are crossing so as to involve risk of collision, the engagement of the crossing rules is not dependent upon the give-way vessel being on a steady course.” And further (para 112): the stand-on vessel need not be on a steady course either. The trigger is steady BEARING (Rule 7(d)(i)), not steady course. An ANS designed to check “is the other vessel on a steady course?” before applying crossing rules will FAIL the UKSC standard. [D-UKSC paras 111–112]
- Resolution: The ANS must use bearing rate of change as the primary trigger for crossing-rule engagement, not course estimation. A vessel that is erratic, slow, manoeuvring, or “waiting” (as ALEXANDRA 1 was) is still subject to crossing rules if the bearing does not appreciably change. The minimum sensor requirement is bearing measurement accuracy over time. Declare in the ConOps: “Crossing rules engage on steady bearing, not steady course, per UKSC [2021] UKSC 6 para 111.” Validate in V&V with scenarios involving erratic-course give-way vessels. [D-UKSC; D-MSC 16.4.2, 16.4.3, Annex 1 §2.7; R]
- Status: Unresolved — no current MASS Code guidance addresses this; requires ANS design change.
- Tag: [D-UKSC paras 77, 80–84, 111–112]; [D-MSC 16.4.2, 16.4.3]; [R]
- Insight D — the “no steady course” holding eliminates a class of ANS errors. If an ANS is designed to check “is the other vessel on a steady course?” before applying crossing rules, it will fail the UKSC standard. The crossing rules engage on steady bearing, not steady course. This means: (a) the ANS must not require course estimation as a precondition; (b) bearing measurement (compass or radar) is the minimum sensor requirement; (c) a vessel that is “waiting” (like ALEXANDRA 1) is still subject to crossing rules if the bearing is steady; (d) this removes the “is she on a course?” ambiguity that Teare J and the Court of Appeal struggled with, which the UKSC resolved as bearing, not course. [D-UKSC paras 77–84, 108–112; R]

#### #29 · Statutory minimum crew and human-presence presumptions (added v0.5, GF-01)

- Legacy: flag-state statute. U.S. example as reported by GAO-24: 46 U.S.C. § 8301(a) (licensed master for vessels propelled by machinery or carrying passengers; licensed mates by tonnage), § 8101(a) (complement stated on the certificate of inspection), § 8102(a) (watchmen on passenger vessels at night), § 8103(a) (U.S. citizens as master, chief engineer and certain watch officers), § 8502 (U.S. pilot in U.S. waters) and § 4312 (engine cut-off switch, which assumes a person aboard). Citations as given in GAO-24 fn. 21–23; not checked against the statutes (GTL-17). [D-GAO24 pp. 12, 19]
- MASS Code: 8.7 and 14.2.1.10–.14 (human master responsible; master aboard if persons are aboard); 14.2.2 (remote operators); 2.3 (modes with persons on board); 6.2 (equivalence to a conventional ship). [D-MSC]
- Friction: The Code describes remote and autonomous operation, but a flag state’s statutes can fix a minimum complement and presume people aboard. GAO-24 reports that the Coast Guard says it cannot waive these minimums for autonomous ships outside the statutory at-sea rocket-recovery pilot (NDAA FY2023 § 11504; pp. 2, 12), that tests may not take crew below the statutory number (p. 10), and that industry told it the inability to go below minimums can make the capital cost of crew-replacing technology impractical (p. 12). MASS 6.2 is an evaluation criterion for approval and does not itself amend a domestic statute, so a MASS could be approved on equivalence grounds and still need the statutory complement. This is the national-layer counterpart of A2 item 4. [D-GAO24 pp. 2, 10, 12; D-MSC 6.2; R]
- Resolution: The ConOps and approval basis should state the statutory complement the flag state requires for each operating mode, how the master and any other statutory roles are met (aboard, or remotely where the statute allows), and the legal route relied on (statutory change, pilot authority, exemption, or none). Submitters should not assume labour savings that the flag state’s statutes do not permit. Flag states with similar statutes may consider whether to seek legislative flexibility before the projected 2032 mandatory date; that is a policy matter outside this bridge. Statutes in other flag states are unsurveyed. [R; S]
- Status: Unresolved — statutory; U.S. data point from mid-2024; later changes not checked (GTL-17).
- Tag: [D-GAO24 pp. 2, 10, 12, fn. 21–23]; [D-MSC 6.2, 8.7, 14]; [R]; [S]; [?]
- Verification update (v0.5.1, VR-03, VR-08): (a) 46 U.S.C. § 8301 as in force on 23 December 2025 applies its minimums to vessels subject to inspection under chapter 33 and excepts vessels operating only on rivers, harbors, lakes (other than the Great Lakes), bays, sounds, bayous and canals; subsection (d) lets the Secretary suspend the chapter during a national emergency proclaimed by the President. The Legacy description above, taken from GAO-24’s summary, is therefore broader than the statute’s scope. (b) GAO’s December 2025 testimony (GAO-26-108762, excerpts only) repeats that the Coast Guard has no waiver authority outside the rocket-recovery pilot. (c) Coast Guard Work Instruction 5P-WI-002(1) of 1 June 2026 tells OCMIs not to set manning below the minimums in 46 U.S.C. § 8301 and 46 C.F.R. Part 15, and says CG-CVC may consider reducing manning below its guideline manning (Marine Safety Manual Vol. III) provided the change complies with law. The statutory floor and the guideline manning above it are different constraints; a Submitter has room to argue only above the floor. The other statutes in Legacy (§§ 8101, 8102, 8103, 8502, 4312) and the pilot’s current status were not re-checked. [D-USC; D-USCG-WI E.3–E.4; D-GAO26T; ?]
- Verification note (v0.5.2, VR-13): the FY2023 NDAA § 11504 at-sea recovery pilot is set out as a note to 14 U.S.C. § 501 (GovInfo 2024 edition); GAO-26-108762 describes it as giving the Coast Guard authority to waive certain crew requirements, and the Coast Guard’s own description lists human supervision of each vessel as a pilot condition. The pilot’s full text, duration and current status were not read. [D-GAO26T; secondary; ?]
- Verification note (v0.6, VR-21): 46 U.S.C. § 8103(a) reads, in substance, that except as otherwise provided in Title 46 only a U.S. citizen may serve as master, chief engineer, radio officer or officer in charge of a deck or engineering watch on a documented vessel; its scope is documented vessels, which is narrower than a general citizenship rule. Chapter 81 headings confirm § 8101 as “Complement of inspected vessels” and § 8102 as “Watchmen”; their text, and §§ 8502, 4312 and 10101, were not read. [D-USC; ?]

#### #30 · Liability presumption for COLREG non-compliance, U.S. Pennsylvania Rule (added v0.5, GF-03)

- Legacy: COLREG Rule 5 look-out and the collision rules generally; U.S. federal maritime negligence doctrine. Under the Pennsylvania Rule, a party to a collision that violated a statute or rule meant to prevent that kind of collision is presumed at fault unless it shows the violation could not have caused the collision (The Pennsylvania, 86 U.S. 125 (1874); Havinga v. Crowley Towing, 24 F.3d 1480 (1st Cir. 1994), as cited in GAO-24 fn. 25; not checked). [D-GAO24 p. 19, fn. 25]
- MASS Code: 16.2 (COLREG compliance); 16.4.2–16.4.3; 9.10 (data logging and authority access). Whether and how the Code addresses civil liability was not checked in this fusion. [D-MSC; ?]
- Friction: GAO-24 (fn. 25) notes that which autonomous technologies satisfy the COLREG look-out requirement may affect civil liability, and that the presumption raises unusual causation questions for autonomous ships: a defective navigation system, an operator improperly engaging or disengaging the system, or a system choosing between outcomes. IMO’s framework work also lists legal liability among its cross-cutting issues (GAO-24 p. 2). An ANS whose look-out equivalence (#1) cannot be shown may therefore carry an evidentiary burden in at least one major admiralty jurisdiction, and the ABIL (Part K) cannot settle liability between private parties. [D-GAO24 p. 2, fn. 25; R]
- Resolution: This bridge gives no legal advice. Practical effect for the approval basis: the look-out equivalence evidence (#1), V&V records (#5, #7, #8, #28) and retained data logs (MASS 9.10; #24) are the material on which a COLREG-compliance dispute would turn, so they should be retained in a form that investigation authorities and counsel can use. Whether the Pennsylvania Rule applies to autonomous vessels in the same way is [?] and needs maritime counsel. [R; ?]
- Status: Open — outside the instrument scope of this bridge; jurisdiction-specific (U.S.).
- Tag: [D-GAO24 p. 2, p. 19 fn. 25]; [R]; [?]
- Verification note (v0.6, VR-19): the Pennsylvania Rule as stated in the 1873-term decision (86 U.S. (19 Wall.) 125) presumes that a statutory violator’s fault was at least a contributing cause, and puts on that vessel the burden of showing the fault could not have been one. Later appellate formulations are softer: the Ninth Circuit describes rebuttal by clear and convincing evidence that the violation could not reasonably be held a proximate cause (MacDonald v. Kahikolu, 581 F.3d 970 (9th Cir. 2009)). Havinga (1st Cir. 1994) was not checked. Whether and how the rule applies to an autonomous vessel’s look-out is a legal question for counsel and is tracked in G-18, not as a verification item. [secondary case-law sources; ?]

### C5. SUPPLEMENTAL FRICTION ROWS (S-1 TO S-4 ADDED IN v0.2; S-5 ADDED IN v0.4; S-6 TO S-8 ADDED IN v0.5)

#### S-1 · Load Lines Convention / 2008 IS Code

- Legacy: Load Lines Convention 1966 as amended by the 1988 Protocol; 2008 IS Code.
- MASS Code: 19.2.1.
- Friction: v0.1 excluded Load Lines, but MASS 19.2.1 explicitly requires compliance with Load Lines and the 2008 IS Code.
- Resolution: Add Load Lines / IS Code compliance to the stability and certification cross-reference; verify operative text externally.
- Status: Open.
- Tag: [D-MSC 19.2.1]; [S/GTL Load Lines]

#### S-2 · MARPOL electronic record books; unmanned non-self-propelled barge exemption

- Legacy: MARPOL 2019 electronic record book amendments; 2021 exemption of unmanned non-self-propelled barges from certain survey/certification requirements.
- MASS Code: 9.10; Ch. 5; Ch. 24.
- Friction: The Status Book lists both; MASS is not the first unmanned-adjacent regulatory issue.
- Resolution: Use the electronic-record and unmanned-barge precedents as analogies only; do not treat them as MASS approval substitutes.
- Status: Analogy only.
- Tag: [D-SB MARPOL entries (79), (84)]; [D-MSC 9.10]; [R]

#### S-3 · 2023–2026 SOLAS / MARPOL amendments not all in force

- Legacy: SOLAS and MARPOL amendments adopted 2023–2026 with future entry-into-force dates.
- MASS Code: Annex 1 (approval basis); 8.2.5; 6.4.2.
- Friction: An approval basis may be proven against a rule version that changes before the mandatory Code enters into force.
- Resolution: Version-lock the approval basis. Maintain an amendment horizon matrix: adopted / accepted / in-force / applicable-to-vessel / approval-basis version, including the 2027 and 2028 future entries.
- Status: Open.
- Tag: [D-SB SOLAS entries (193), (216), (220)–(223); MARPOL PROT 1997 entries (28)–(29)]; [D-MSC 6.4.2, 8.2.5]; [R]

#### S-4 · MASS Code application gate

- Legacy: (applies across all instruments).
- MASS Code: 2.1.
- Friction: The Code applies only when the Administration deems other instruments impracticable or insufficient. v0.1 treated scope too automatically.
- Resolution: Record the application-gate decision in the MASS Record / approval basis: which instruments are insufficient, why the Code applies, and which chapters are invoked.
- Status: Open.
- Tag: [D-MSC 2.1, 5.1.3, Appendix certificate checkboxes]; [R]

#### S-5 · COLREG rule-switching trigger at channel entrances (added v0.4, RT-03)

- Legacy: COLREG Rules 9, 15–17; UKSC [2021] UKSC 6. Rule 9(a) (narrow channels); Rules 15–17 (crossing); UKSC para 145 (“shaping to enter” test). [D-UKSC; D-HET §6.3]
- MASS Code: 16.4.2 (situational awareness: perception, comprehension, projection); 16.4.3 (collision avoidance based on risk assessment); 8.2 (ConOps); Annex 1 §2.7 (V&V plan). [D-MSC]
- Friction: The UKSC has provided an authoritative (in UK law), sensor-observable trigger for COLREG rule-switching at narrow channel entrances. No MASS Code guidance, flag-state circular or classification society rule addressing the same trigger was identified in the supplied sources (flag-state and class practice is unsurveyed; GTL-15). The ANS needs a three-phase rule-switching state machine (K4) to comply with both COLREG and the UKSC interpretation; without one it cannot determine, on a defensible basis, when to switch from crossing rules to narrow channel rules. [D-UKSC para 145; D-MSC 16.4.2, 16.4.3; R; ?]
- Resolution: Adopt the three-phase rule-switching state machine (K4) as a proposed ANS design requirement for any MASS operating near narrow channels. Encode it in the ConOps, validate it in V&V, and declare it in the regulatory gap analysis. The “shaping to enter” test is, in the supplied sources, the first judicially articulated, sensor-implementable rule-switching trigger available for autonomous navigation (see K1, Insight B). [D-UKSC; D-MSC Annex 2 §8.2; R; S — proposed design rule]
- Status: Unresolved — proposed design rule; no IMO or flag-state guidance was identified.
- Tag: [D-UKSC paras 134–145]; [D-MSC 16.4.2, 16.4.3, Annex 2 §8.2]; [R]; [S]

#### S-6 · Version-locked approval basis vs iterative software change (added v0.5, GF-15)

- Legacy: (applies across the approval route.)
- MASS Code: 6.4.2 and 8.2.5 (re-assessment on change); Annex 1 (approval basis). K3 of this bridge states that any change to the ConOps, OE, software or ROC requires re-assessment. [D-MSC; R]
- Friction: GAO-26 (Snapshot) reports that commercial companies develop robotic autonomous systems iteratively and outpace the Navy’s fixed-requirements, linear approach, and that iterative processes let them fold in the latest technology updates. A software-heavy MASS updated on a commercial cadence meets an approval basis that is version-locked (S-3, K3). The tension is derived by this bridge from the two sources; GAO-26 does not discuss maritime regulation. [D-GAO26 Snapshot; D-MSC 6.4.2, 8.2.5; R]
- Resolution: The approval basis should declare a change-control classification: which software and parameter changes (for example detection thresholds, S-5 values) need re-assessment, which are pre-approved within declared bounds, and what evidence supports each. Whether an Administration will accept bounded pre-approval is [?]; no flag-state practice was surveyed. [R; S; ?]
- Status: Open — derived tension.
- Tag: [D-GAO26 Snapshot]; [D-MSC 6.4.2, 8.2.5]; [R]; [S]; [?]

#### S-7 · Crew-executed certifications converted to software-executed, military precedent (added v0.5, GF-12)

- Legacy: Navy certification of ships and crews before operational use (GAO-22 p. 33). [D-GAO22]
- MASS Code: 5 (surveys and certificates); 16.4.2–16.4.3 (ANS functions). [D-MSC]
- Friction: GAO-22 (p. 33) reports that a key effort for uncrewed vessels is converting checks once done by the crew into checks executed by software, and that this will take several years. It also reports (pp. 32–34) that Navy prototyping plans named the certifications needed without saying how prototypes would be used to develop them, and that late changes to meet a certification requirement could delay delivery. Commercial MASS face a parallel conversion where crew checks that underpin SOLAS and COLREG compliance become ANS or ROC functions (#1, #14, #15). Analogy only: the Navy’s certification regime is not the IMO’s. [D-GAO22 pp. 32–34; R]
- Resolution: Use as a prompt in the approval basis: list the crew-performed checks and certifications that the ANS or ROC now performs, and state when evidence for each will be produced. No ABIL entry. [R]
- Status: Analogy only.
- Tag: [D-GAO22 pp. 32–34]; [R]

#### S-8 · U.S. automated-vessel crew-substitution precedent (added v0.5, GF-06)

- Legacy: 46 C.F.R. § 15.715 (automated vessels, 1987) and 46 C.F.R. § 62.50-30 (periodically unattended machinery plants, 1988), as cited in GAO-24 fn. 12–14; the Coast Guard’s Marine Safety Manual Volume III approval process. [D-GAO24 pp. 10, 18]
- MASS Code: 6.2; Annex 1. [D-MSC]
- Friction: Per GAO-24 (p. 10), these rules let automated systems replace specific engineering-department crew based on the system’s capability, its demonstrated and continuing reliability, and a maintenance programme, and they correspond to IMO’s first degree of autonomy (fn. 13). They are the closest existing U.S. regulatory precedent for substituting automation for crew on evidence of reliability, and the Coast Guard says autonomous operations must still meet statutory minimum crew (#29). [D-GAO24 pp. 10, 18; R]
- Resolution: Use only as an analogy for how equivalence evidence is framed (capability, demonstrated reliability, maintenance). It is not a MASS approval substitute (compare S-2). [R]
- Status: Analogy only.
- Tag: [D-GAO24 p. 10, fn. 12–14]; [R]

## PART D — GAP REGISTER

Severity summary: 6 HIGH (G-1, G-2, G-3, G-5, G-9, G-16); 14 MEDIUM (G-4, G-6, G-7, G-8, G-10 to G-15, G-17 to G-20); 0 LOW. G-1 to G-12 originate in v0.1; G-13 to G-15 were added in v0.2; G-16 to G-20 were added in v0.5. “Linked” fields are a v0.3 navigation aid. [R]

#### G-1 · Small MASS below core application — HIGH

- Instruments: MASS Code, SOLAS, COLREG.
- Evidence: Res. §3 invites application of the Code to MASS under 500 GT “as far as practicable.” [D-MSC]
- Justification: Small autonomous craft may operate in COLREG waters without a dedicated IMO MASS framework.
- Proposed resolution: Flag-state small-MASS rules; future IMO small-MASS guidance; ConOps rule-set declaration.
- Linked: #6, B5 (Unrated). Tag: [D]; [R]
- GAO fusion (v0.5): Canada and the UK have national small-autonomous-vessel measures (#6); GAO-24 (p. 10) reports the Coast Guard had issued no autonomous-specific regulation since 1987–88 and handled testing case by case. [D-GAO24 pp. 8–10; ?]
- Verification leads (v0.5.2, VR-14): versions of the Coast Guard Authorization Act of 2025 (S. 524, passed by the Senate in March 2025; H.R. 4275, passed by the House in July 2025) include a pilot program for governance and oversight of small uncrewed maritime systems and a permanent NOAA seat on AutoPoCo; the Coast Guard Work Instruction cites FY2026 NDAA § 7331 for NOAA small unmanned systems of 35 feet or less. Enactment and final text of the Authorization Act were not checked; these are leads, not findings. [?]

#### G-2 · Lights / shapes / sound-signal verification — HIGH

- Instruments: COLREG, MASS Code.
- Evidence: MASS 16.2 requires COLREG compliance; Part III has no dedicated lights/shapes/sound-signal chapter. [D-MSC]
- Justification: Safety-critical signalling may be compliant in principle but unverified for unmanned activation.
- Proposed resolution: Add an automated-signalling and survey checklist to MASS approval and the ConOps.
- Linked: #5, #10, G-11. Tag: [D]; [R]; [GTL]

#### G-3 · Human intervention latency — HIGH

- Instruments: COLREG Rule 2, MASS Code 8.7.
- Evidence: MASS 8.7.4 requires “ample time and sufficient information” with no numeric latency; COLREG Rule 17 requires action as soon as it becomes apparent. [D-MSC; D-HET]
- Justification: Collision avoidance and fallback are time-critical.
- Proposed resolution: Define phase-specific maximum latency and handover time in the ConOps; validate in V&V and risk assessment [D-MSC Ch. 7].
- Linked: #2, #7, B3 (Fractured). Tag: [D]; [R]
- GAO fusion (v0.5, GF-08): stakeholders flagged technical difficulty when control is passed back and forth between operators and autonomous systems (GAO-24 p. 5); the IMO one-ROC-at-a-time agreement (p. 7) makes handover timing a design point. [D-GAO24 pp. 5, 7; R]

#### G-4 · Sensor sufficiency threshold — MEDIUM

- Instruments: COLREG Rule 7, MASS Code.
- Evidence: HET quotes “scanty information”; the Code requires adequate situational awareness but sets no sensor threshold. [D-HET; D-MSC 16.4.2]
- Justification: The threshold depends on sensor suite, OE and encounter type.
- Proposed resolution: Declare minimum sensor / confidence thresholds and degraded-state triggers in the OE/ODD.
- Linked: #4, #9. Tag: [D]; [R]; [?]

#### G-5 · 2026–2032 voluntary transition — HIGH

- Instruments: All.
- Evidence: MASS 1.2.4 (non-mandatory, though developed to facilitate a future mandatory status); Annex 17 target of 1 January 2032. [D-MSC]
- Justification: Guidance may be used unevenly while legacy duties remain mandatory.
- Proposed resolution: National adoption (flag states may make the Code mandatory nationally), contract/class requirements, flag-state approval conditions, explicit certificate annotations.
- Linked: B7 (T2), S-3, S-4. Tag: [D]; [R]
- GAO fusion (v0.5, GF-05): GAO-24 (pp. 7–8) reports the IMO committee Chair saying the mandatory date was uncertain and that the non-mandatory framework had to be right first time because changes after approval would be hard; the head of the U.S. delegation agreed. This supports treating 2026–2032 as the period in which approval-basis practice sets precedent. [D-GAO24 pp. 7–8; R]

#### G-6 · MARPOL annex-by-annex bridge absent — MEDIUM

- Instruments: MARPOL, MASS Code.
- Evidence: The Code has environmental goals but no MARPOL annex-specific verification chapter. [D-MSC contents; R]
- Justification: Pollution obligations remain applicable, but operational verification for unmanned spaces is not mapped.
- Proposed resolution: Add a MARPOL compliance annex to the ConOps / MASS Record and automate records and reporting. The Code could reference MARPOL explicitly, or MARPOL could be amended for unmanned engine rooms and automated discharge monitoring (IMO process, outside this document’s scope; see BR-02).
- Linked: #20–#24, S-2. Tag: [D]; [R]; [GTL]
- Verification update (v0.5.1, VR-10): IMO’s MASS page reports that the Legal Committee agreed a road map on possible amendments or interpretations of its treaties, that the FAL Committee will assess the Code against the FAL Convention annex, and that the PPR Sub-Committee is tasked with a regulatory scoping exercise and gap analysis of MEPC instruments, including the Code. That is the IMO process for the MARPOL side of this gap; no output from it was found when the pages were read. [D-IMO; ?]

#### G-7 · ROC fatigue / watchkeeping implementation — MEDIUM

- Instruments: STCW, MASS Code.
- Evidence: MASS 14.2.1.8–.9 addresses fatigue/rest; 14.2.2.3 requires sufficient remote operators, time, resources and procedures. [D-MSC]
- Justification: The gap is not absence of fatigue principles; it is ROC-specific quantification and enforcement across working regimes. STCW A-VIII/1 is written for seafarers, not remote operators. [S/GTL]
- Proposed resolution: Adopt a ROC watchkeeping standard, rest-hour records, workload limits and a multi-MASS alarm-load assessment.
- Linked: #19, GTL-10. Tag: [D]; [R]; [GTL]
- GAO fusion (v0.5, GF-04, GF-10): the IMO working-group agreement that one master may be responsible for several ships in some circumstances (GAO-24 p. 7) raises the multi-MASS alarm-load question; GAO-22 (p. 16) notes the Navy had not determined how many sailors uncrewed systems need ashore or aboard crewed hosts. [D-GAO24 p. 7; D-GAO22 p. 16; R]

#### G-8 · Military / government autonomous vessels — MEDIUM

- Instruments: MASS Code, COLREG, SOLAS.
- Evidence: MASS 2.1.2 excludes warships, naval auxiliaries and other government non-commercial ships. [D-MSC] COLREG Rule 1 covers vessels generally, but government vessels may claim sovereign immunity. [S/GTL]
- Justification: Military MASS may interact with civilian MASS while outside the Code.
- Proposed resolution: Separate military assurance; voluntary flag-state alignment; civil-military encounter protocols. No resolution exists within the IMO framework.
- Linked: B5 (Exempt). Tag: [D]; [R]
- GAO fusion (v0.5, GF-14 to GF-16): GAO-26 reports the Navy intends a hybrid fleet with large and small expendable autonomous systems in all domains (letter p. 1; Snapshot), and GAO-22 (p. 14) reports a 2020 plan for 143 uncrewed of 546 total vessels and vehicles by 2045 (dated). Military and civil MASS may share waters while only civil MASS fall under the Code; no GAO text addresses civil-military encounter rules. GAO-26 (p. 2, fn. 5) also records that the FY2026 NDAA repealed the 2021 provision on the acquisition executive agent for autonomy and defined a portfolio acquisition executive (GTL-22). [D-GAO22 p. 14; D-GAO26 pp. 1–2; ?]

#### G-9 · Cyber compromise as navigation-compliance dependency — HIGH

- Instruments: COLREG, MASS Code.
- Evidence: MASS 9.8, 10.3, 12.3–12.6, 17.2.10 address cyber/security; COLREG compliance depends on functioning perception and action. [D-MSC; D-HET; R]
- Justification: A cyber event can degrade situational awareness or control and cause navigational non-compliance (e.g., degraded look-out under Rule 5). The linkage is an inference; the instruments do not state it. [R]
- Proposed resolution: Link cyber risk assessment to COLREG-critical functions; define cyber-induced degraded/fallback states.
- Linked: #1, B3 (Usurped), Part F, BR-05. Tag: [D]; [R]
- GAO fusion (v0.5, GF-08): GAO-24 (p. 6) reports many stakeholders and the literature rating cyber risk substantial for autonomous ships, with some saying risk rises when no human aboard can troubleshoot. [D-GAO24 p. 6]

#### G-10 · Non-cooperative targets — MEDIUM

- Instruments: COLREG, MASS Code.
- Evidence: MASS 16.4.3 requires risk-based collision avoidance; it does not show performance against violating or deceptive targets (pirate vessels, AIS-disabled vessels, vessels in violation of COLREG). [D-MSC; R]
- Justification: Real encounters include non-compliant, deceptive or sensor-obscured vessels.
- Proposed resolution: Scenario-based V&V for non-cooperative targets; ConOps limits and escalation rules; declare the ANS’s capability for such scenarios.
- Linked: #7, #8. Tag: [R]; [?]
- GAO fusion (v0.5, GF-08): a shipbuilder’s concern about a kayaker in a harbour not visible to cameras (GAO-24 p. 5) is an example of a small, non-AIS, hard-to-detect target. [D-GAO24 p. 5; R]

#### G-11 · Restricted-visibility sound signals — MEDIUM

- Instruments: COLREG Rule 35, MASS Code.
- Evidence: HET/COLREG excerpts establish the sound-signal issue; the Code lacks dedicated implementation detail. [D-HET; D-MSC contents; R]
- Justification: Unmanned operation does not remove the signalling duty.
- Proposed resolution: Automated Rule 35 signal activation on detection of restricted visibility; fault monitoring; survey test; specify in the ConOps and validate during surveys.
- Linked: #10, G-2. Tag: [R]; [GTL]

#### G-12 · Specification plurality: international / inland / national — MEDIUM

- Instruments: COLREG, national law.
- Evidence: HET notes International Rule 28 versus Inland §83.28 [Reserved]; inside the U.S. COLREG demarcation lines the Inland Navigation Rules (33 CFR Part 83) apply. [D-HET]
- Justification: Rule-set switching at demarcation lines can change compliance obligations; a MASS in U.S. waters may face both rule sets.
- Proposed resolution: The ConOps must declare the rule set by voyage phase and geography; V&V must test transitions. This is a genuine DOF that must be bounded.
- Linked: GTL-07. Tag: [D-HET]; [R]; [GTL]

#### G-13 · Load Lines / IS Code omitted from v0.1 — MEDIUM

- Evidence: MASS 19.2.1 expressly references Load Lines and the 2008 IS Code. [D-MSC]
- Proposed resolution: Add Load Lines / IS Code compliance mapping and external text verification.
- Linked: S-1, GTL-11. Tag: [D]; [R]

#### G-14 · Amendment-version drift — MEDIUM

- Evidence: The Status Book lists 2026 SOLAS amendments entering into force in 2028 and MARPOL Annex VI 2026 amendments entering into force in 2027. [D-SB]
- Proposed resolution: The approval basis must specify the rule version and update triggers.
- Linked: S-3. Tag: [D]; [R]

#### G-15 · Application-gate ambiguity — MEDIUM

- Evidence: MASS 2.1 applies the Code when the Administration deems other instruments impracticable or insufficient. [D-MSC]
- Proposed resolution: Record the Administration’s application-gate decision and invoked chapters in the MASS Record.
- Linked: S-4. Tag: [D]; [R]

#### G-16 · Statutory minimum crew vs crew-reduced MASS — HIGH

- Instruments: flag-state statute, MASS Code (8.7, 14), SOLAS.
- Evidence: GAO-24 pp. 2, 10, 12 (U.S.): statutes fix minimum crew; the Coast Guard says it cannot waive them outside the rocket-recovery pilot; industry says this may make crew-replacing technology uneconomic. [D-GAO24]
- Justification: A MASS approved under the Code may be unable to operate with fewer people than a statute requires, and the Code’s mandatory form (projected 2032) does not by itself amend national statutes.
- Proposed resolution: ConOps statement of the statutory complement per mode; flag-state legislative review; pilot-style authority where available.
- Linked: #29, A2 item 8, S-8. Tag: [D-GAO24]; [R]; [?]

#### G-17 · No accepted reference evidence for look-out equivalence — MEDIUM

- Instruments: COLREG Rule 5, MASS Code 16.4.2.
- Evidence: GAO-24 p. 13: the Coast Guard says it needs examples of autonomous look-out technology to decide how to verify compliance; stakeholders have not shared any; the reasons it gives include immaturity, proprietary designs and the cost of meeting crew minimums. [D-GAO24]
- Justification: Without shared reference evidence each Submitter argues Rule 5 equivalence from scratch (#1) and each Administration judges it without a benchmark.
- Proposed resolution: Declare the equivalence argument and test results in the approval basis. Flag states and class societies may consider publishing anonymized reference test protocols; this bridge does not assert that any exists.
- Linked: #1, #25, G-18, GTL-18. Tag: [D-GAO24]; [R]; [?]

#### G-18 · Liability allocation for ANS-attributable collisions — MEDIUM

- Instruments: COLREG, national admiralty law.
- Evidence: GAO-24 p. 2 (liability among IMO cross-cutting issues) and fn. 25 (Pennsylvania Rule; causation factors). [D-GAO24]
- Justification: The instruments say little about private liability, and admiralty presumptions can turn on COLREG compliance.
- Proposed resolution: Retain compliance evidence (#30); obtain maritime counsel; monitor the IMO Legal Committee, which GAO-24 (p. 7) lists among the committees active on autonomous ships.
- Linked: #30, #24, GTL-19. Tag: [D-GAO24]; [R]; [?]
- Verification note (v0.6, VR-19): the doctrinal statement is confirmed (see #30); application to autonomous vessels is OPEN-COUNSEL and cannot be closed by research. [?]

#### G-19 · Remote-operation staffing and lifecycle cost basis unquantified — MEDIUM

- Instruments: STCW, MASS Code 14, flag-state law.
- Evidence: GAO-22 pp. 15–17: Navy operations-and-sustainment costs for uncrewed systems not estimated; crew numbers undetermined; earlier Navy crew reduction by automation raised maintenance cost and led to added crew when automated systems failed (as GAO reported in 2017 and 2021). GAO-24 p. 6: stakeholders divided on training cost and workforce effects. [D-GAO22; D-GAO24]
- Justification: An approval basis may rest on staffing and fatigue assumptions (G-7, #19) with no cost or workload evidence. GAO-22 shows this failure pattern in a military setting; transfer to commercial MASS is by analogy only.
- Proposed resolution: Declare the ROC staffing basis, fallback staffing for automation failure, and workload assumptions in the ConOps; validate alarm load in V&V.
- Linked: G-7, #19, #29. Tag: [D-GAO22]; [D-GAO24]; [R]

#### G-20 · Approval-basis change cadence — MEDIUM

- Instruments: MASS Code 6.4.2, 8.2.5, Annex 1.
- Evidence: MASS 6.4.2 and 8.2.5 [D-MSC]; GAO-26 Snapshot on iterative development [D-GAO26].
- Justification: See S-6: a version-locked basis meets software that changes on a commercial cadence.
- Proposed resolution: Change-control classification in the approval basis (S-6, K2).
- Linked: S-3, S-6, K3. Tag: [D-MSC]; [D-GAO26]; [R]; [?]

## PART E — INVARIANT SET: WHAT THE BRIDGE PRESERVES

**FRAMING PRINCIPLE.** MASS 6.2: “The basic principle for the evaluation criteria should be to ensure a level of safety, security and environmental protection that is expected of a conventional ship.” [D-MSC 6.2] This is not merely one invariant among many. It is the equivalence standard the Code applies to the evaluation of every friction point in this bridge. For every COLREG friction, the question is not “does the MASS comply with the literal text?” but “does the MASS achieve the level of safety expected of a conventional ship?” This means: (a) human sensory terms (“sight and hearing”) need not be replicated literally if sensor fusion achieves equivalent or superior safety; (b) the “readily apparent” standard (Rule 8) need not be visual if digital signalling achieves equivalent legibility; (c) the “scanty information” prohibition (Rule 7) is satisfied if the ANS’s uncertainty quantification is at least as conservative as a prudent human officer. Every invariant below is subordinate to this principle. [D-MSC 6.2; R]

Reconciliation note (v0.4) [R]: MASS 6.2 states the Code’s evaluation criterion for approval. It does not amend COLREG, SOLAS or MARPOL, and it is guidance until the Code is made mandatory (A2). The equivalence arguments in (a) to (c) are therefore arguments the Submitter makes and the Administration accepts, through the approval basis and regulatory gap analysis (K1); they are not a relaxation of the mandatory legacy text during the transition.

Tag: [D-MSC 6.2; R]

| # | Invariant | Source | Preservation status | Caveat | Tag |
| --- | --- | --- | --- | --- | --- |
| 1 | Safety, security and environmental protection equivalent to a conventional ship | MASS 6.2; 1.3.1 | Preserved as evaluation criterion (the Framing Principle above) | Non-mandatory until adopted / implemented | [D-MSC]; [R] |
| 2 | Human master responsible at all times | MASS 8.7.3; 14.2.1.10 | Preserved | If persons are on board, master physically on board; only one master at a time | [D-MSC] |
| 3 | COLREG compliance for navigation | MASS 16.2 | Preserved as requirement in Code | Operative COLREG verification partly external | [D-MSC]; [GTL] |
| 4 | SOLAS safety-of-navigation compliance | MASS 16.2; 16.3.3; 9.10.6 | Preserved and supplemented | Operative SOLAS text partly external | [D-MSC]; [GTL] |
| 5 | MARPOL pollution-prevention compliance | MASS Preamble 5–6; environmental purpose; MARPOL status | Preserved by implication and general international-law conformity | No annex-by-annex MASS verification mapping | [D-MSC]; [R]; [GTL] |
| 6 | Human oversight and ability to override | MASS 8.7.1; 10.7; 16.5 | Preserved | Latency and HMI effectiveness require V&V | [D-MSC]; [R] |
| 7 | ISM / ISPS management and security | MASS 5.7–5.8; 11; 12 | Preserved and extended to ROC | ROC management may use alternative certification | [D-MSC] |
| 8 | STCW-level competence for remote operators | MASS 14.2.2.1; 14.4.2 | Preserved as level-not-less-than principle | STCW applicability and rest details require external verification | [D-MSC]; [GTL] |
| 9 | OE / fallback safety boundary | MASS 8.3–8.5; 13.4.1 | Preserved | Thresholds must be declared and tested | [D-MSC]; [R] |
| 10 | Data logging and authority access | MASS 9.10.1–9.10.6 | Preserved | Data availability is not identical to incident reporting | [D-MSC]; [R] |

The Invariant-Testing result remains PARTIAL / MODERATE because textual preservation does not equal enforceable preservation during the non-mandatory transition. [R]

## PART F — CONNECTION TO HETEROGENEITY UNDER OBSERVABILITY (HET)

### F1. HET CONCEPT MAPPING

| HET concept | Corrected IMO bridge application | Source | Tag |
| --- | --- | --- | --- |
| A₁ class-attacking adversary | Public compliance documentation, common MASS designs and shared rule interpretations may permit class-level exploit development without capturing a deployed MASS. | HET §2 | [D-HET]; [R] |
| A₂-hybrid (capture-then-exploit) | A captured MASS or compromised ROC may expose ANS firmware, thresholds, keys or models for reuse against variants. HET cites the seizure of a U.S. Navy underwater glider by China on 15 December 2016 as a documented precedent (refs R1, R2); not independently verified here (GTL-13). | HET §2 | [D-HET]; [R] |
| A₂-pure (real-time) | Live probing, spoofing, jamming or transient cyber effects may bypass the value of static implementation diversity. | HET §2, §4.3 | [D-HET]; [R] |
| H_d_variant | The variant fraction whose cheapest critical path is adversary-independent after the independence test and minimum-path reduction. Not a general “diversity score.” | HET §7.2 | [D-HET] |
| Apparent vs genuine DOF | Different vendor labels do not prove independent exploit paths; different thresholds or sensor architectures may or may not be genuine depending on transfer. Distinguish, for example, different ANS vendors with one COLREG interpretation (apparent) from different Rule 17 thresholds or sensor-fusion architectures (potentially genuine). | HET §6.2 | [D-HET]; [R] |
| Hidden centralization | A shared ANS stack, training data, keys, ROC, update channel or generator can collapse diversity. | HET §4.6 Scene 4 | [D-HET] |
| Topology-adjusted capture | A compromised ROC or shared maintenance channel may reach multiple variants; k_cap matters. | HET §4.6 Scene 5 | [D-HET]; [R] |
| Invariant extension | COLREG compliance must survive sensor degradation, environmental drift and calibration band, not just nominal test cases. | HET §5; MASS 8.3, 9.12 | [D-HET]; [D-MSC]; [R] |
| Model–reality residual | ANS compliance is proven against a model; the residual between model and reality is where collisions happen and must be declared and validated. The Code’s testing and validation [9.12] sets no acceptable residual. | HET §8.3; MASS Annex 1 §2.7 | [D-HET]; [D-MSC]; [R] |

### F2. CORRECTED HIDDEN-CENTRALIZATION FINDING

If all vessels in a fleet use the same ANS implementation for a COLREG-critical function, and that implementation is the cheapest critical exploit path, then the fleet can have H_d_variant = 0 for that exploit path. [D-HET §7.2; R]

But a shared specification or shared in-envelope behaviour is not priced by node-level H_d_variant. HET explicitly excludes specification-level and in-envelope exploitation from H_d_variant and says those mechanisms apply by construction across variants. [D-HET §4.6 mechanism (e)/(j), §12 L10] Therefore:

- “Same ANS software stack” may be a node-level hidden centralization. [R]
- “Same COLREG interpretation” may be specification-level commonality, not H_d_variant itself. [R]
- Both must be disclosed, but they are different mechanisms. [R]

### F3. RECOMMENDED HETEROGENEITY EVIDENCE FOR MASS APPROVAL

A MASS approval package should include, at minimum:

1. ANS / remote-navigation software supply-chain dependency map. [R]

2. Shared ROC, communication, update, key-management and cloud-service dependencies. [R]

3. Variant-family description if multiple vessels share a design family. [R]

4. H_d_variant analysis only if a variant family and exploit paths are defined; otherwise report UNMEASURED, not a number. [D-HET §7; P1]

5. k_cap / topology disclosure where one ROC or maintenance channel can affect multiple MASS. [D-HET §4.6 Scene 5; R]

6. Specification-level commonality disclosure for COLREG interpretation, Rule 17 thresholds, Rule 2 departure logic and restricted-visibility behaviour. [D-HET §12 L10; R]

7. V&V evidence for degraded sensors, calibration drift and environmental drift. [D-HET §5; D-MSC 9.12; R]

8. Disclosure of any shared autonomy architecture, integration or test environment, or common data repository adopted across vessels or vendors (F6). [D-GAO22 pp. 3, 5, 30; R]

### F4. FLEET-LEVEL OBSERVATION

The regulatory gap analysis [D-MSC Annex 2 §8.2] is a per-vessel document and, as read here, does not address fleet-level heterogeneity. [R] The software supply-chain diversity of a flag state’s fleet is therefore invisible to it. v0.1 recommended that flag states require heterogeneity across their MASS fleets; v0.2 narrowed this to disclosure of shared dependencies, and v0.3 and v0.4 keep the narrower form because H_d_variant is unmeasured here and the HET protocol is proposed, not run. [D-HET §9.7; R] No empirical HET protocol has been run in this document.

### F5. REGULATORY k_cap (added v0.4, RT-09)

The MASS Code’s dual-certificate architecture creates a regulatory k_cap. MASS 5.3.1: “Every ROC should, for each MASS it operates, have a valid MASS ROC Certificate.” MASS 5.6.2: “Where a MASS ROC Certificate is withdrawn or ceases to be valid, the Administration should review the effect on the associated MASS Safety Certificate as well as on other MASS ROC Certificates issued for this ROC.” [D-MSC 5.3.1, 5.6.2] A single ROC operating multiple MASS creates a many-to-one certification topology. If the ROC fails (cyber compromise, connectivity loss, personnel failure), all associated MASS certificates are affected simultaneously. This is HET’s k_cap in regulatory form: a compromised or failed ROC can reach k_cap MASS at once. The Code requires the Administration to “review the effect” but does not mandate redundancy or limit k_cap per ROC. [D-MSC; D-HET §4.6 Scene 5; R]

Proposal [S]: flag states could consider requiring ROC redundancy, or limiting or disclosing k_cap per ROC. This stays within F4’s disclosure-first posture; v0.3 deliberately narrowed v0.1’s prescriptive recommendation (J5 item 11), and the amendment file’s stronger wording (“should require”) is carried here as a proposal, not a finding. The ConOps should specify k_cap and the fallback arrangements. [D-HET §4.6 Scene 5; S]

v0.5 note (GF-04). The IMO working-group agreements reported in GAO-24 (p. 7) add a second many-to-one link at the human level: a master may be responsible for several ships, while one remote operating centre may be responsible for a ship at any one time. A ROC fault reaches every ship it operates (certificate topology above); a master’s overload can reach every ship that master covers (G-7). Both counts belong in the k_cap and fallback disclosure. [D-GAO24 p. 7; R]

### F6. COMMON-ENABLER ARCHITECTURES: EFFICIENCY VERSUS HETEROGENEITY (added v0.5, GF-11)

GAO-22 (pp. 3, 5, 30) reports that the Navy plans much of its digital infrastructure (an autonomy architecture, a rapid autonomy integration lab, data repositories) to be common to all its major uncrewed efforts, so that vehicles and software from several contractors work to the same rules. GAO-26 (Snapshot) reports the Navy’s stated aim of common, platform-agnostic enabling capabilities that free resources. GAO-22 (p. 23) also reports that several early vehicles did not conform to the planned architecture, which could mean costly retrofits. [D-GAO22 pp. 3, 5, 23, 30; D-GAO26 Snapshot]

Read through HET (F1, F2) [R]: a shared autonomy architecture is deliberate commonality. If code, models or the update channel are shared, it is node-level hidden centralization (F2). If only an interface standard is shared, it is specification-level commonality, which H_d_variant does not price (F2). Commonality lowers retrofit cost and integration risk (the GAO point) and also widens the set of ships that one exploit or fault can reach (F5). The two goals pull against each other. Neither GAO report analyses the cyber or adversarial resilience of the common architecture. This bridge states the tension; it does not measure it (GTL-14).

Relevance to civil MASS [R]: the same tension appears if flag states or class societies converge on one interpretation, one test suite or one ROC supplier. F3 item 8 adds disclosure; no heterogeneity requirement is proposed (F4). Limits: military-programme evidence; the HET protocol has not been run. [D-HET; R]

## PART G — RED-TEAM AND CORRECTION RECORD

### G1. v0.1 BR FINDINGS AND DISPOSITION

| ID | Severity | v0.1 finding | v0.1 resolution | Disposition in v0.2 / v0.3 / v0.4 |
| --- | --- | --- | --- | --- |
| BR-01 | HIGH | MASS Code provisions were cited as [D] but the Code is non-mandatory until 2032; treating them as binding overstates their authority. | All Code citations note non-mandatory status; authority derives from SOLAS/COLREG/MARPOL; the Code is guidance until Ch. XVI is in force. | Applied. Authority disclaimer, transition status and roadmap distinction (A2, reading convention). |
| BR-02 | HIGH | The bridge did not address the tacit-acceptance amendment procedure; COLREG amendments need a two-thirds majority of Parties present and voting, with a one-third objection threshold [COLREG Art. VI, as cited in v0.1; verify, GTL-04]. | The bridge proposes no COLREG amendments; gaps are resolved via the gap analysis, flag-state implementation or ConOps declarations. COLREG text changes are outside scope. | Applied. SOLAS Art. VIII, COLREG Art. VI and MARPOL Art. 16 included in B2/B3; no direct COLREG amendment proposal. BR-02 expanded at v0.4: the COLREG procedure is four-stage (proposal and circulation, MSC adoption, Assembly adoption, entry into force absent objection by more than one-third), not a single two-thirds / one-third rule; COLREG is practically frozen until at least 2032. See B2. [D-SB; R] |
| BR-03 | MEDIUM | Friction #10 (Parts C/D not addressed) may be wrong: MASS 5.1.5 issues the MASS Safety Certificate in addition to SOLAS I/12 certificates, and 16.2 requires COLREG compliance. | Partially resolved: the gap is how Parts C/D are verified for unmanned vessels, not whether COLREG applies. | Applied. Reframed as a verification/implementation gap (#10, G-2). |
| BR-04 | MEDIUM | The bridge assumed the Ever Smart UKSC decision is authoritative globally; it is UK law, not IMO interpretation. | The decision is one jurisdiction’s interpretation; the ANS must implement the flag state’s interpretation, declared in the ConOps. | Applied. Retagged [S/GTL], jurisdiction-specific (#25). |
| BR-05 | MEDIUM | G-9 (cyber = COLREG non-compliance) is an inference [R]; the Code addresses cyber but does not link it to COLREG compliance. | G-9 tagged [R]; the linkage is proposed, not in current text. | Applied. [D] for cyber requirements, [R] for the compliance dependency (G-9). |
| BR-06 | LOW | The SG read did not test whether the amendment loop is truly Balancing or could be Reinforcing. | Acknowledged. SOLAS 223 entries in about 52 years against COLREG 7 in about 54 years is roughly 32:1, which suggests Balancing for SOLAS/MARPOL and possibly stalled for COLREG. | Applied. “Balancing intended”; reinforcing complexity acknowledged (B4). |
| BR-07 | LOW | Load Lines and STCW-F are not addressed. | Acknowledged; scope limited to SOLAS, COLREG, MARPOL and the Code. | Partly applied. Load Lines added (S-1, G-13); STCW-F remains out of scope except as an external ledger item. |

### G2. CORRECTIONS APPLIED IN v0.2 (CARRIED)

| ID | Correction | Where in v0.4 and v0.5 |
| --- | --- | --- |
| C-01 | Added literal Purpose and τ | A1 |
| C-02 | Added authority disclaimer | A2 |
| C-03 | Added source limitations: Status Book is not consolidated operative law | A3 |
| C-04 | Corrected MASS 2.1 application gate | A2, S-4, G-15 |
| C-05 | Corrected master-location rule when persons are on board | B3, #2 |
| C-06 | Corrected STCW rest/fatigue overstatement | #19, G-7 |
| C-07 | Corrected MARPOL Annex IV/V “no crew = no waste” overstatement | #21, #22 |
| C-08 | Added Load Lines / IS Code row | S-1, G-13 |
| C-09 | Added amendment-version drift row | S-3, G-14 |
| C-10 | Added HET specification-level caveat | F2 |
| C-11 | Added full SG closure markers and SG limitations | A3, B9 |
| C-12 | Removed “12th confirmation” as established SG fact | B8 |
| C-13 | Corrected “only mechanism” claim for the regulatory gap analysis | B7 |
| C-14 | Corrected remote-operator / SSO overstatement | #17 |

### G3. ROUND 3 AMENDMENTS APPLIED IN v0.4 (RT-01 TO RT-10; INSIGHTS A–D)

Source: Round 3 fresh-context red-team audit, recorded in the MRB v0.4 Amendment File under the date 11 November 2026 (see J6 item 1). [R]

| ID | Severity | Amendment | Applied at |
| --- | --- | --- | --- |
| RT-01 | HIGH | Correct the #25 Ever Smart characterization to the UKSC three-phase test; GTL-08 confirmed | C4 #25; Part H (GTL-08); Part I |
| RT-02 | HIGH | Add the “no steady course” holding as new row #28 | C4 #28; C0; K2 |
| RT-03 | HIGH | Add S-5, the rule-switching trigger at channel entrances | C5 S-5; C0; K2; K4 |
| RT-04 | MEDIUM | Elevate MASS 6.2 to a framing principle | Part E preamble |
| RT-05 | MEDIUM | Correct and expand the COLREG amendment procedure (BR-02 expansion) | B2; BR-02 (G1); A2 item 7 |
| RT-06 | MEDIUM | Add the ABIL concept and mapping | Part K (K1–K3) |
| RT-07 | MEDIUM | Split the Rule 17(a)(ii) and 17(b) triggers | C1 #7 and #8 |
| RT-08 | LOW | Add the temporal dimension to “readily apparent” | C1 #5 |
| RT-09 | LOW | Add the regulatory k_cap propagation note | F5 |
| RT-10 | LOW | Add the agent/responsibility asymmetry | B3 (ANS entry) |
| Insight A | — | Regulatory Interpretation Layer as a new maritime concept (ABIL) | K1 |
| Insight B | — | UKSC “shaping to enter” as a design threshold | K1; S-5 |
| Insight C | — | COLREG amendment freeze window | A2 item 7 |
| Insight D | — | “No steady course” eliminates a class of ANS errors | C4 #28 |

### G4. v0.5 GAO FUSION ITEMS (GF-01 TO GF-16)

Source: the three GAO documents supplied for the v0.5 build, read in full and cited by page. These items record what was taken from GAO and where it was applied. They are not red-team dispositions. [R]

| ID | Source | What GAO reports | Applied at |
| --- | --- | --- | --- |
| GF-01 | GAO-24 pp. 2, 10, 12; fn. 21–23 | U.S. statutes fix minimum crew and credentials; Coast Guard says it cannot waive them outside the rocket-recovery pilot | A2 item 8; B2; #29; G-16; K2; GTL-17 |
| GF-02 | GAO-24 pp. 5, 13 | IMO look-out position as reported; no examples of autonomous look-out technology shared; compliance method not established | A2 item 7; #1; #25; G-17; GTL-18 |
| GF-03 | GAO-24 p. 2, fn. 25 | Pennsylvania Rule and causation questions for autonomous ships | #30; G-18; K2; GTL-19 |
| GF-04 | GAO-24 p. 7 | IMO working-group agreements on master, ROC and multi-ship responsibility | B3; F5; G-7; #26 |
| GF-05 | GAO-24 pp. 2, 7–8 | IMO timeline as of May 2024; Chair’s caution; first-time-right | A2 item 3; G-5; GTL-02 |
| GF-06 | GAO-24 pp. 10–11, 13–14, 18; Table 1 | Coast Guard practice: case-by-case approvals, equivalents, policy letters, AutoPoCo, rulemaking threshold | B2; B3; K1; K3; L3; S-8; GTL-20 |
| GF-07 | GAO-24 pp. 8–10, 16, 18 | Canada, Norway and UK measures; Yara Birkeland crew five to three; Japan and South Korea did not respond | #5; #6; #10; #19; G-1; GTL-15; GTL-21 |
| GF-08 | GAO-24 pp. 5–6 | Stakeholder views: handover, small hard-to-see people, cyber, physical security, labour | B3; #1; #17; #19; G-3; G-9; G-10 |
| GF-09 | GAO-24 pp. 3–4, Fig. 2 | IMO degrees of autonomy | A4 |
| GF-10 | GAO-22 pp. 15–17 | Operations and sustainment not estimated; crew numbers undetermined; optimal-manning outcome | G-7; G-19; #19 |
| GF-11 | GAO-22 pp. 3, 5, 17, 23, 30 | Common digital infrastructure; architecture non-conformance; infrastructure funded far below vehicles | F3; F6; B5 |
| GF-12 | GAO-22 pp. 32–34 | Crew-to-software certification conversion; prototyping plans lack certification detail | S-7 |
| GF-13 | GAO-22 pp. 26–31 | No measurable prototype criteria; no integrated schedule; concurrency risk | B5; K3; L4 |
| GF-14 | GAO-22 pp. 19–26; GAO-26 Snapshot | Portfolio management and governance; unformalized stakeholder roles | #26; L4 |
| GF-15 | GAO-26 Snapshot; p. 2 fn. 5 | Domain-siloed approach; iterative development; PAE consolidation; NDAA FY2026 changes | S-6; G-8; G-20; L4; GTL-22 |
| GF-16 | GAO-22 pp. 3–5, 14; GAO-26 p. 1 | Scale and role of military uncrewed and autonomous systems outside the Code | G-8; B5 (Exempt) |

Considered and not applied: GAO-22’s shipbuilding-plan dollar figures beyond the illustrative uses above; GAO-22’s Navy recommendations and agency comments (pp. 34–37, 43–46), which concern Navy programme management; GAO-24’s environmental-benefit and rocket-recovery droneship detail beyond #29; GAO-26’s classified-report background. [R]

## PART H — GROUND TRUTH LEDGER

The following claims require external verification before legal, certification or operational reliance. “Status” shows what is verifiable from the supplied sources.

| GTL ID | Claim | Current status | Concrete verification method |
| --- | --- | --- | --- |
| GTL-01 | Official MASS Code adoption, effect date, non-mandatory status (including Res. §3 on MASS under 500 GT) | CLOSED-VERIFIED (v0.6). The official resolution text on imo.org reads “Resolution MSC.595(111) (adopted on 21 May 2026)”, as Annex 16 to MSC 111/22/Add.1; MSC 111 sat 13–22 May 2026; effect on 1 July 2026 and non-mandatory status are stated in the MSC 111 report and national circulars; the invitation on MASS under 500 GT was confirmed on IMO pages [D-IMOP; D-IMO]. Summaries that say 22 May give the session’s closing day | None. A2 item 2 stands. |
| GTL-02 | Mandatory MASS Code target of 1 Jan 2032 via SOLAS XVI | CLOSED-RESCOPED (v0.6): verified as a roadmap target, not law. [D-MSC Annex 17] roadmap; GAO-24 p. 7 reports the same 2032 effective-year target as of May 2024 (GF-05); IMO-side summaries say 1 January 2032 at the earliest and that it may be revisited [D-IMO]. Becomes standing tracking item T-1, not a verification item | T-1: track MSC 112 (December 2026), SOLAS Chapter XVI adoption text and entry-into-force amendments. |
| GTL-03 | SOLAS amendment count of 223 entries through MSC 111 | [D-SB] verified as Status Book list | Confirm against the official IMO treaty database and consolidated SOLAS amendment register. |
| GTL-04 | COLREG seven amendment entries through 2013 (and Art. VI amendment mechanics) | [D-SB] verified as Status Book list | Confirm against the official IMO treaty database and consolidated COLREG text. |
| GTL-05 | MARPOL 90 entries under the 1978 Protocol and 29 under the 1997 Protocol | [D-SB] verified as Status Book list | Confirm against the official IMO treaty database; distinguish adopted, accepted, in-force and applicable amendments. |
| GTL-06 | Operative COLREG Rules 1, 2, 5–10, 15–17, 19, 20–37, Part F (Rules 39–41) | Expanded at v0.4: Rules 2, 5, 6, 7, 8, 9, 15, 16, 17 and 19 are cross-checked against UKSC- and HET-quoted text. Rules 1, 10, 20–37 and 39–41 remain unverified [S/GTL]. | Verify against the official consolidated COLREG text and amendments through A.1085(28). The UKSC and HET quotations are not the consolidated text. |
| GTL-07 | Rule 28 international vs U.S. Inland §83.28 [Reserved] | CLOSED-VERIFIED (v0.6): 33 C.F.R. § 83.28 is “[Reserved] (Rule 28)” in the eCFR-derived tables (Cornell LII listing; eCFR PDF current to 24 June 2024; a 2025 section listing), and the Coast Guard Navigation Center amalgamation marks Rule 28 as International Rules only [D-HET claim confirmed] | None. Re-check only if 33 C.F.R. Part 83 is amended. |
| GTL-08 | Evergreen Marine (UK) Ltd v Nautical Challenge Ltd [2021] UKSC 6 and its Rule 9 / Rules 15–17 holding | CONFIRMED (closed). Recorded by the Round 3 audit as verified against the full UKSC judgment text; the holding is a three-phase test, not a binary (RT-01). Carried as recorded; the judgment was not re-opened for v0.4 or v0.5. | None outstanding beyond jurisdictional scoping: the judgment is UK law (I2 item 2). |
| GTL-09 | SOLAS V/19, V/20, V/33, V/34, XI-1/6, I/12 operative text | MASS references [D-MSC]; operative text [S/GTL] Remains [S/GTL]: SOLAS operative text still not supplied; MASS Code references confirmed. | Verify against consolidated SOLAS 1974 as amended. |
| GTL-10 | STCW A-VIII/1 and remote-operator rest/watchkeeping applicability | [S/GTL] Remains [S/GTL]: STCW text not supplied. | Verify the STCW Convention/Code, flag-state guidance and any IMO MASS/STCW circulars. |
| GTL-11 | Load Lines / 2008 IS Code operative requirements | MASS 19.2.1 reference [D-MSC]; text [S/GTL] Remains [S/GTL]: Load Lines / IS Code text not supplied; MASS 19.2.1 reference confirmed. | Verify the Load Lines Convention / 1988 Protocol and consolidated 2008 IS Code. |
| GTL-12 | MARPOL Annex I/IV/V/VI and Protocol I applicability to a specific MASS mode | [S/GTL] Remains [S/GTL]: MARPOL operative text not supplied beyond the Status Book. | Verify consolidated MARPOL annexes, flag acceptance, ship type, tonnage, voyage, persons on board and national implementation. |
| GTL-13 | Chinese seizure of U.S. Navy glider, 15 Dec 2016 | CLOSED-VERIFIED (v0.6): seizure on 15 December 2016 about 50 nautical miles northwest of Subic Bay, from USNS Bowditch’s survey, by PLA Navy vessel 510; returned on 19 December 2016. Official sources: DoD releases NR-448-16 and NR-451-16 and the 20 December 2016 statement; USNI News and Reuters corroborate [D-DOD] | None. |
| GTL-14 | H_d_variant predicts adversary acquisition cost | HET hypothesis; protocol not run | Run the HET §9 pilot or an independent equivalent; report measured time-to-compromise and analyst-dependence range. |
| GTL-15 | Small-MASS flag-state practice | CLOSED-RESCOPED (v0.6): the claim is narrowed to the four jurisdictions now checked: United States (Coast Guard case-by-case practice and the 1 June 2026 Work Instruction), Canada (Tier I policy), United Kingdom (SI 2023/1216 and Workboat Code Edition 3) and Norway (RSV 12-2020) [D-USCG-WI; D-TC; D-UKSI; D-NMA]. Japan and South Korea did not respond to GAO; other flag states unsurveyed | Residual survey of other flag states is OPEN-EXTERNAL and is tracked in G-1. |
| GTL-16 | Actual ROC cyber topology / k_cap / shared dependencies | [?] | Inspect architecture, supply-chain SBOM, key-management plan, update channels and ROC network diagrams; run a red-team capture exercise. |
| GTL-17 | U.S. minimum-crew and credential statutes (46 U.S.C. §§ 8301, 8101, 8102, 8103, 8502, 4312, 10101) and the Coast Guard no-waiver position, including the rocket-recovery pilot (NDAA FY2023 § 11504) | OPEN-DOABLE (v0.6): § 8301 read [D-USC]; § 8103(a) text confirmed; chapter 81 headings for §§ 8101 and 8102 confirmed; Coast Guard no-waiver position repeated December 2025 [D-GAO26T] and in WI 5P-WI-002(1) E.3 [D-USCG-WI]; pilot basis located as a note to 14 U.S.C. § 501. NOT read: text of §§ 8101, 8102, 8502, 4312, 10101; pilot text and status; changes after December 2025 | Read the remaining sections and the pilot text on uscode.house.gov or GovInfo. |
| GTL-18 | IMO position that look-out (COLREG Rule 5) applies to autonomous ships and the international rule need not be amended now; Coast Guard view that compliance method is not established | OPEN-DOABLE (v0.6): MSC.1/Circ.1638 (3 June 2021) read through annex page 66. Section 6.7 and Table 3 class COLREG as high-priority and give option I for degree one, I–II for degrees two and three and II for degree four [D-IMOP]. So the “no COLREG amendment” position reported by GAO-24 is a later IMO decision, not the scoping outcome. NOT read: the COLREG appendix of Circ.1638 (after page 66) and the MSC 108–111 records of the later decision | Read the COLREG entry in Circ.1638 Appendix 2 and agenda item 5 of the MSC 108 to 111 reports (MSC 111/22/Add.1 is the latest). |
| GTL-19 | Pennsylvania Rule and its application to autonomous-vessel collisions | CLOSED-VERIFIED for the doctrine (v0.6): The Pennsylvania, 86 U.S. (19 Wall.) 125 (1873 term, often cited 1874), presumption and “could not have been” burden confirmed; softer later formulations noted in #30. Havinga (1st Cir. 1994) not checked. Application to autonomous vessels is OPEN-COUNSEL and moves to G-18 | None for the doctrine. Counsel for application (G-18). |
| GTL-20 | Coast Guard Policy Letters 22-01 (Change 1), 01-20 and 01-23; Marine Safety Manual Vol. III; 46 C.F.R. §§ 15.715 and 62.50-30; equivalency provisions | OPEN-DOABLE (v0.6): Policy Letter 22-01 (Change 1) is cancelled by Coast Guard Work Instruction 5P-WI-002(1) of 1 June 2026 [D-USCG-WI, read in full]. Policy Letters 01-20 and 01-23, Marine Safety Manual Vol. III and 46 C.F.R. §§ 15.715 and 62.50-30 NOT checked | Verify the remaining items on Coast Guard and eCFR sources. |
| GTL-21 | Canada Tier I small-autonomous-ship policy (2022); UK Merchant Shipping (Small Workboats and Pilot Boats) Regulations 2023 changes (December 2023); Norwegian Maritime Authority guidance (2020); Yara Birkeland crew reduction | CLOSED-RESCOPED (v0.6): Canada Tier I Policy TP 13585 [D-TC] and UK SI 2023/1216 [D-UKSI] confirmed in excerpts; Norwegian circular RSV 12-2020 of 27 August 2020 confirmed (applies to autonomy levels 3–5 on domestic voyages; uses the IMO equivalence process) and Yara Birkeland’s reduction to three crew confirmed by NMA material [D-NMA]. Residual minor points: Canada’s distinct-signal requirement (#5), UK Workboat Code Annex 2 text (#10), Yara’s hoped-for crew of two | Residual points are low-materiality OPEN-DOABLE items under #5, #10 and #19. |
| GTL-22 | Navy RAS organization and statute changes reported by GAO-26: portfolio acquisition executive for RAS (2025); repeal of FY2021 NDAA § 218 and 10 U.S.C. § 1732 definition via Pub. L. No. 119-60 | OPEN-DOABLE (v0.6): Pub. L. 119-60 signed 18 December 2025; § 1802(a) added 10 U.S.C. § 1732 (portfolio acquisition executive), confirmed in the codified text’s source note; § 811 repeals many earlier NDAA provisions (law-firm summaries). The repeal of FY2021 NDAA § 218 by § 811(b) rests on GAO-26 only | Read § 811(b) in the public law text; confirm current Navy organization. |

v0.4 status note: GTL-08 is closed (confirmed) and GTL-06 is expanded, both as recorded by the Round 3 audit and not independently re-verified in this fusion. GTL-09 to GTL-12 remain [S/GTL]. GTL-01 to GTL-05, GTL-07 and GTL-13 to GTL-16 are unchanged from v0.3. [R]

v0.5 status note: GTL-17 to GTL-22 are added; GTL-02 and GTL-15 are annotated; all other items are unchanged from v0.4. The GAO documents themselves were read and cited by page in this build; what they cite (statutes, cases, circulars, IMO and foreign-regulator documents) is not verified. [R]

v0.5.1 and v0.5.2 status note: GTL-01, GTL-02, GTL-17, GTL-18, GTL-20, GTL-21 and GTL-22 were narrowed or corrected in verification round 1 and its continuation (Part M). No GTL item is closed. GTL-19 was not examined. [R]

v0.6 status note: round 2 closed GTL-01, GTL-07, GTL-13 and the doctrinal part of GTL-19 against primary or official sources, rescoped GTL-02, GTL-15 and GTL-21, and corrected the reading of GTL-18. Every ledger item now has a disposition in M5. [R]

v0.1 ledger mapping (v0.1 had 8 items; none is lost): v0.1-1 COLREG count → GTL-04; v0.1-2 SOLAS count → GTL-03; v0.1-3 MARPOL count → GTL-05; v0.1-4 Code effective date → GTL-01; v0.1-5 mandatory 2032 → GTL-02; v0.1-6 Ever Smart → GTL-08; v0.1-7 glider → GTL-13; v0.1-8 MASS under 500 GT status → GTL-01. [R]

## PART I — PEER-REVIEW READINESS AND τ SELF-CHECK

### I1. WHAT v0.5 SATISFIES

| Requirement | Status |
| --- | --- |
| Purpose declared | Yes |
| τ declared and testable | Yes |
| Build State present and current for v0.5 | Yes |
| Non-mandatory MASS Code status stated | Yes |
| Transition-period gap stated | Yes |
| Private-analysis authority disclaimer | Yes |
| At least 10 friction points with evidence, resolution and tag | Yes |
| 30 core rows (#1–#28 retained; #29–#30 added) | Yes |
| Eight supplemental rows (the five in v0.4, plus version lock versus iterative change, crew-to-software certification analogy, U.S. automated-vessel precedent) | Yes |
| Epistemic tags corrected for external law and missing operative text | Yes |
| SG limitations declared; SG closure markers present | Yes |
| HET mapping corrected for H_d_variant limits | Yes |
| Ground Truth Ledger carried (22 items; GTL-08 closed, GTL-06 expanded, GTL-17 to GTL-22 added in v0.5) | Yes |
| Complete without v0.1, v0.2, v0.3, v0.4 or the amendment file | Yes |
| Ever Smart holding correctly characterized as three-phase test | Yes (RT-01) |
| “No steady course” holding incorporated | Yes (RT-02, #28) |
| Rule-switching state machine specified | Yes (S-5, K4), as a proposed design rule [S] |
| MASS 6.2 elevated to framing principle | Yes (RT-04) |
| COLREG four-stage amendment procedure stated | Yes (RT-05) |
| ABIL concept named and mapped | Yes (Part K) |
| Rule 17(a)(ii) vs 17(b) trigger distinction made | Yes (RT-07) |
| Temporal dimension of “readily apparent” stated | Yes (RT-08) |
| Regulatory k_cap identified | Yes (RT-09, F5) |
| Agent/responsibility asymmetry stated | Yes (RT-10) |
| COLREG freeze window declared | Yes (Insight C, A2 item 7), as a practical not a legal freeze |
| Gap Map recounted after fusion | Yes, incrementally (B10); full recount pending at audit |
| GAO evidence fused and traceable (GF-01 to GF-16) | Yes (G4, Part L) |
| GAO citations checked against the supplied PDFs | Yes, in this build; what GAO cites is not checked (GTL-17 to GTL-22) |
| U.S.-centred and military evidence declared as such | Yes (B9, L1, L5) |
| Additions to existing rows labelled as v0.5 GAO fusion | Yes |
| Independently verified | No — UNAUDITED (v0.5 itself not independently audited) |

### I2. WHAT REMAINS UNRESOLVED BEFORE EXTERNAL SUBMISSION

1. Official consolidated COLREG / SOLAS / MARPOL / STCW / Load Lines text must be checked for every operative rule citation (GTL-06, GTL-09 to GTL-12). COLREG Rules 2, 5–9, 15–17 and 19 are cross-checked against UKSC- and HET-quoted text only, which is not the consolidated text. [GTL]
2. Ever Smart / UKSC: the holding was verified at Round 3 (GTL-08 closed). Open: jurisdictional scoping. The judgment is UK law, persuasive elsewhere; which interpretation other flag and coastal states apply is unsurveyed. [?]
3. Flag-state implementation practice for small MASS and ROC watchkeeping must be surveyed (GTL-15, GTL-10). [GTL]
4. HET claims remain structural / proposed until a pilot is run. [D-HET §9.7]
5. Citation carry-over. The v0.4 and v0.5 fusions did not re-open MSC.595(111), the Status Book, SG, BP, HET or the UKSC judgment. Every [D-…] citation and paragraph number is carried from v0.1, v0.2, v0.3 and the Round 3 amendment file as written and has not been re-checked in v0.4 or v0.5. This includes the new D-UKSC paragraph numbers and the MASS 4.1, 5.1.3.4, 5.3.1, 5.6.2, 6.2, 8.7.3, 14.2.1.10, Annex 1 §1.4/§2.5 and Annex 2 §8.2 citations. Re-check them in the fresh-context audit. [R]
6. S-5 is a proposed design rule [S]. Its numeric thresholds (S5.5, S5.6) are engineering proposals, no flag state, classification society or IMO body has validated it, and K4 records specification gaps found at fusion. [S]
7. The K2 document-location section numbers (for example “ConOps §4.3”) and the “MSMD” expansion are carried from the amendment file and are unverified navigation aids. [R; ?]
8. The B10 recount is incremental; a from-scratch recount is due at audit. [R]
9. v0.6 requires a fresh-context audit because the producing session cannot certify its own artifact. [D-BP §V1]

10. GAO evidence is dated: GAO-22 is April 2022, GAO-24 is August 2024 and predates the MASS Code, and GAO-26 summarizes a March 2025 report. Later changes to U.S. statutes, Coast Guard policy, IMO documents and foreign regulators’ measures are unchecked (GTL-17 to GTL-22). [?]

11. GAO-24 is U.S.-centred; Canada, Norway and the UK appear only as GAO reports them and Japan and South Korea are absent. Do not generalise to other flag states (GTL-15, GTL-21). [?]

12. Part L, S-7, S-8 and F6 use military-programme findings by analogy. They do not show how commercial MASS or the IMO process will behave. [R]

13. Verification round 1 (Part M) closed or narrowed some items using public web sources and one primary Coast Guard document. Everything not listed in Part M is still unverified, and GTL-19 was not examined. [R]

14. Round 2 set a disposition for every ledger item (M5). Five items remain open-doable and nine open-external; the nine are declared limits that need the Architect’s source files or outside work. [R]

### I3. τ SELF-CHECK — NON-CERTIFYING

A reader can locate at least 10 friction points, each with cited evidence, a proposed resolution and a tag: #1 look-out / sensor fusion; #2 responsibility / remote-master latency; #3 safe speed / OE; #4 scanty information / sensor threshold; #5 manoeuvre legibility and decision timing; #7 stand-on observation threshold; #8 stand-on prediction; #10 lights / shapes / sound signals; #13 SOLAS equipment by electronic means; #17 ISPS / ROC security; #19 STCW remote operators; #20 MARPOL Annex I unmanned machinery spaces; #23 Annex VI emissions; #25 Rule 9 vs crossing rules at channel entrances; #28 bearing, not course; S-1 Load Lines; S-3 amendment-version drift; S-5 rule-switching trigger; #29 statutory minimum crew; #30 liability presumption; S-6 approval-basis change cadence. [D/R]

A reader can also name at least one earlier analysis error. v0.1 tagged the Ever Smart judgment [D] although it was not in the supplied anchor sources; v0.3 retagged it [S/GTL]; v0.4 retags it [D-UKSC] after Round 3 verification. v0.1 and v0.3 also summarized the holding as a binary (crossing rules apply while crossing a channel, Rule 9 within it); the UKSC holding is a three-phase test turning on whether the approaching vessel is shaping to enter on final approach (RT-01). Further errors are listed in J5. v0.5 adds an omission found while reading the GAO material: v0.1 to v0.4 treated national implementation as one undifferentiated layer and did not map domestic minimum-crew statutes or liability doctrine (#29, #30). [R]

This self-check is not a fresh-context certification. [D-BP §V1]

## PART J — LINEAGE AND CONSOLIDATION RECORD

### J1. ARTIFACT BLOCK

| Field | Value |
| --- | --- |
| Artifact | MASS Regulatory Bridge v0.6 |
| Date | 10 November 2026 |
| Protocol | Build Protocol v1.0 |
| Grammar | Structural Grammar v1.0 |
| Primary sources | MSC.595(111); Status Book 2026 Vol I; SG v1.0; BP v1.0; Heterogeneity Under Observability; UKSC [2021] UKSC 6 (all carried via v0.1 to v0.4 and the Round 3 amendment file; none re-opened for v0.5); GAO-22-104567, GAO-24-107059 and GAO-26-109014 (read in full and cited by page in v0.5); v0.5.1 adds IMO web pages, 46 U.S.C. § 8301 text, Coast Guard Work Instruction 5P-WI-002(1), IHO standards pages and GAO-26-108762 excerpts (Part M); v0.6 adds the MSC.595(111) resolution cover pages, MSC.1/Circ.1638 annex pages 1–66, DoD releases on the 2016 glider seizure, Norwegian Maritime Authority material and case-law sources on the Pennsylvania Rule |
| Supersedes | MASS Regulatory Bridge v0.1, v0.2, v0.3, v0.4, v0.5, v0.5.1 and v0.5.2, and the MRB v0.4 Amendment File |
| Build State | IN CYCLE — verification round 2 applied; audit pending |
| External audit | Round 3 dispositions carried from v0.4. Independent audit of v0.5 pending. |
| Fusion producer | Claude (Anthropic AI model), at the Architect’s direction. The producing session cannot certify the artifact. [D-BP §V1] |
| Hash | Not computed for this document. SHA-256 of the source files is recorded in J2 and J8. |
| Silent drops | None known. Deliberate removals and supersessions are listed in J5; fusion reconciliations are listed in J7 and J8. |

### J2. SOURCE FILE RECORD

| File | Internal title | Size | Lines | SHA-256 |
| --- | --- | --- | --- | --- |
| MASS_REGULATORY_BRIDGE_v0_1.txt | IMO REGULATORY BRIDGE v0.1 | 44,539 bytes | 546 | da0548750730d67db3fe2c6725ca527bdf49d6386e93cd353541b94396e2de56 |
| MASS_REGULATORY_BRIDGE_v0_2.txt | THE MASS REGULATORY BRIDGE v0.2 (dated 11 November 2026) | 52,988 bytes | 1,067 | 76b3f8fad0616dc945000841f0c7e997b00da8c25dead3081c954d02b8385203 |
| THE_MASS_REGULATORY_BRIDGE_v0_3.md | THE MASS REGULATORY BRIDGE v0.3 | 84,075 bytes | 1,361 | 41d8f6278e162c2a9640bf41a4451318a49203e0348c2d6e3cd38c89184a0205 |
| MRB_v0_4_AMENDMENT.md | MASS REGULATORY BRIDGE v0.4 AMENDMENT FILE | 43,049 bytes | 615 | 0e554d608745d083ac426861b59bcbf091d6d525c1dd003b8d0ec5048fa4e7c3 |
| MASS_REGULATORY_BRIDGE_v0_4.md | THE MASS REGULATORY BRIDGE v0.4 | 147,480 bytes | 1,357 | 7cfaba801c33765c35179af87af3f29687b2878b576fd5c062eebd7fc8bc5fd4 |
| gao-22-104567.pdf | GAO-22-104567, Uncrewed Maritime Systems (April 2022) | 5,807,930 bytes | n/a (PDF) | 99d930786cb9a2f70c58483805a7b5b9cff992747a758b736b22e9fa21de7401 |
| gao-24-107059.pdf | GAO-24-107059, Coast Guard: Autonomous Ships and Efforts to Regulate Them (August 2024) | 1,199,706 bytes | n/a (PDF) | 9c22abbfda25966d2888c197a0d2b760b0c88307b69364541b22bc7318d46ba0 |
| gao-26-109014.pdf | GAO-26-109014, Robotic Autonomous Systems (June 2026) | 655,557 bytes | n/a (PDF) | c6302cb70a2e02953e427da53f13ba8b1d576da91e3c58e681e2c566844bb117 |
| MASS_REGULATORY_BRIDGE_v0_5.md | THE MASS REGULATORY BRIDGE v0.5 | 203,449 bytes | 1,659 | 661919c27af1644b5adfd3a40fbae3df03610fcfa9ade1d55dca3a865e6e72e2 |
| MASS_REGULATORY_BRIDGE_v0_5_1.md | THE MASS REGULATORY BRIDGE v0.5.1 | 218,885 bytes | 1,734 | e6dc1e96a8c3e262438534fa5edb2ecb46cf77fe279b09ba4308fbc839be45ea |
| MASS_REGULATORY_BRIDGE_v0_5_2.md | THE MASS REGULATORY BRIDGE v0.5.2 | 225,404 bytes | 1,757 | fdaa6d138e55580e5a622b9c598c3bb9f534083048779e1513f89fc52836e529 |

The v0.1 and v0.2 records are carried from v0.3. The v0.3 and amendment records were computed on the files as uploaded for the v0.4 fusion; their line counts include the final unterminated line (`wc -l` reports 1,360 and 614). All four files use CRLF line endings, with table cells flattened to one cell per line.

The v0.4 and GAO records were computed on the files as uploaded for the v0.5 build.

### J3. CONSOLIDATION RULES USED (v0.3 FUSION, CARRIED)

1. Where v0.2 corrected v0.1, v0.2 controls.

2. Where v0.2 compressed v0.1 analysis and the detail is not contradicted, v0.1 detail is restored (J4).

3. Restored COLREG operative detail is re-tagged under v0.2’s tag discipline: [D-HET] only where HET quotes the rule, otherwise [S/GTL].

4. All IDs (#1–#27, S-1–S-4, G-1–G-15, BR-01–BR-07, C-01–C-14, GTL-01–GTL-16) are preserved unchanged.

5. The Gap Map counts were not recomputed.

6. New in v0.3 as organizational aids only [R]: Document Map, Glossary, Matrix Index (C0), per-row Status field, Gap Register “Linked” field, v0.1 ledger mapping, this Part J.

The v0.4 fusion rules and reconciliations are recorded in J7. Rule 5 above (Gap Map counts not recomputed) is superseded by the B10 recount. [R]

### J4. RESTORED FROM v0.1 (ABSENT OR COMPRESSED IN v0.2) — CARRIED FROM v0.3

Agency failure modes (B3); Preamble 6 quotation (B2); amendment-ratio note (B4); Rule 5 misapplication detail (B5); sensor-to-sense mapping (#1); fallback-response interval and MASS 8.4.2 (#2); cliff-not-gradient (#3); degraded-state alert (#4); AIS/VDES and Part D appliance points (#5); Rule 10(j) (#6); CPA/TCPA threshold and ConOps / Annex 1 validation (#7); prediction-accuracy escalation (#8); Rule 19 specific obligations (#9); MASS 5.1.5 (#10); ISM quadrilateral (#18); Ever Smart holding summary (#25); responsibility chain (#26); four verification layers (#27); MASS Ch. 7 reference (G-3); sovereign-immunity point (G-8); non-cooperative target examples (G-10); Inland Rules context (G-12); Navy glider example (F1); fleet-level observation (F4); original BR resolutions (G1); v0.1 ledger mapping (Part H).

### J5. DELIBERATE REMOVALS AND SUPERSESSIONS

| # | Prior content | Treatment in v0.3 / v0.4 / v0.5 | Basis |
| --- | --- | --- | --- |
| 1 | “SOLAS Chapter I applies to ships ≥500 GT” as the scope test | Replaced by the MASS 2.1 scope and application gate | v0.2 correction |
| 2 | Regulatory gap analysis as “the only mechanism” | One integration mechanism among several | C-13 |
| 3 | Remote operator “replaces the Ship Security Officer” | Transferred responsibilities; no automatic SSO replacement | C-14 |
| 4 | “No crew = no sewage / garbage” | Conditionally applicable | C-07 |
| 5 | No IMO-level ROC fatigue standard | Principles exist; ROC-specific implementation is the gap | C-06 |
| 6 | Greimas “12th confirmation” | Candidate post-v1.0 instance | C-12 |
| 7 | Ever Smart tagged [D] | [S/GTL], jurisdiction-specific | BR-04 |
| 8 | Master may always be at the ROC | Master must be on board when persons are on board | C-05 |
| 9 | Claim that a flag state without MASS Code surveys “will fail its COLREG Part F audit” | Not carried: an unsupported prediction, and absent from v0.2 | v0.3 decision |
| 10 | Strict verification hierarchy (III Code → Part F → XI-1 → Ch. 5) | Four distinct layers; no hierarchy asserted | v0.2 #27 |
| 11 | Recommendation that flag states require ANS heterogeneity | Disclosure only (F4) | v0.2 Part 4 |
| 12 | IMO committee process as a fifth substrate | Procedural mechanism | v0.2 B2 |
| 13 | Open/Recurse risk state “Dormant” | “Live” | v0.2 B5 |
| 14 | “IMO should develop a mandatory small MASS code” | “Future IMO small-MASS guidance” | v0.2 G-1 |
| 15 | Gap Map 47 : 12 : 6 (65) | v0.2 map 34 : 18 : 14 (66), carried | v0.2 |
| 16 | Purpose and τ “as declared above” | Literal Purpose and τ | C-01 |
| 17 | v0.1 / v0.3 #25 summary: “first UKSC decision on COLREG in about 45 years”, crossing rules apply where a vessel crosses a channel, Rule 9 governs vessels within a channel | Replaced by the UKSC para 145 three-phase test; the “first decision in about 45 years” claim is not carried | RT-01 |
| 18 | #25 status “Jurisdiction-specific; unverified”; GTL-08 tagged [S/GTL] | “Verified; jurisdiction-specific (UKSC); operationalizable as ANS design threshold”; GTL-08 confirmed and closed | RT-01; amendment Part 5 |
| 19 | v0.3 BR-02 summary of COLREG Art. VI as a single two-thirds / one-third rule | Expanded to the four-stage procedure | RT-05 |
| 20 | Amendment-file wording “mandatory ANS design requirement” (RT-03, S5.1) | “Proposed design requirement” / “proposed ANS logic” | Fusion reconciliation R-3 |
| 21 | Amendment-file Insight B wording “first legally binding ANS decision threshold”; “no IMO guidance, flag-state circular or class rule provides this” | “Authoritative in UK law, persuasive elsewhere”; “first identified in the supplied sources”; flag-state and class practice unsurveyed | R-4 |
| 22 | “COLREG text frozen until at least 2032”; “6-year window” | “Practically frozen”; “about five years”; an Art. VI amendment remains possible | R-5 |
| 23 | RT-04 wording “the legal equivalence standard that governs every friction point” | “The equivalence standard the Code applies to evaluation”, with a transition-period caveat | R-6 |
| 24 | Amendment-file F5 “Flag states should require ROC redundancy or limit k_cap” | Reworded as a proposal [S], consistent with item 11 | R-11 |
| 25 | v0.4 B10 Gap Map 42 : 27 : 18 (87) | Superseded by the v0.5 map 56 : 37 : 24 (117) | v0.5 recount |
| 26 | v0.4 GTL-15 “[?]” | Annotated as partial: Canada, Norway and UK as reported by GAO; open for other flag states | GF-07 |
| 27 | v0.4 B3 Administration row read as Single / institutional | Retained, with a one-flag-state inference that U.S. practice is Plural / distributed | GF-06 |
| 28 | v0.4 G-8 evidence (exclusion and sovereign immunity only) | Extended with GAO-22 and GAO-26 scale and governance evidence | GF-14 to GF-16 |
| 29 | v0.4 Part I counts (28 core rows, five supplemental, 16 GTL items) and “v0.4 requires a fresh-context audit” | 30, eight, 22; audit requirement moved to v0.5 | v0.5 |
| 30 | v0.5 K1 and L3 description of Policy Letter 22-01 (Change 1) as current Coast Guard guidance | Marked superseded by Work Instruction 5P-WI-002(1); the v0.5 text is kept and followed by a verification update | VR-05 |
| 31 | v0.5 K4 S5.6 “ENC accuracy per IHO S-44” | Replaced: S-44 is the hydrographic survey standard; ENC product specifications are S-57 and S-101 | VR-06 |
| 32 | v0.5 #29 scope of 46 U.S.C. § 8301 taken from the GAO-24 summary | Narrowed to the statute’s scope and exceptions; statutory floor distinguished from guideline manning | VR-03 |
| 33 | v0.5.1 GTL-21 “not checked” for the Canadian and UK items | Canadian Tier I policy and UK SI 2023/1216 confirmed from excerpts; Norway, Yara and the Canadian distinct-signal point stay open | VR-11, VR-12 |
| 34 | v0.5 A2 item 7 and L2 reading that IMO’s scoping outcome supports no COLREG amendment | Qualified: Circ.1638 Table 3 lists COLREG as high-priority with option II for degree four; “no amendment” is treated as a later decision not yet traced | VR-16 |
| 35 | v0.5 #30 statement of the Pennsylvania Rule standard | Kept; later, softer formulations and the 1873-term citation added | VR-19 |
| 36 | v0.5.2 GTL-01, GTL-07, GTL-13 statuses | Closed against official sources | VR-15, VR-17, VR-18 |
| 37 | v0.5.2 J6 item 19 “verification queue” | Replaced by the M3 remaining queue and the M5 closure dispositions | M3, M5 |

### J6. ITEMS FOR ARCHITECT DECISION

1. Date. The Round 3 audit record and the amendment file are dated 11 November 2026, and v0.2 is also dated 11 November 2026 (carried from v0.3). v0.4 is dated 10 November 2026, its build date. The discrepancy is recorded here, not silently corrected. Confirm the intended dates.

2. Round count and status. The amendment file instructs Round count “3 of 3 (audit round)” and Status “IN CYCLE — round 3 complete”, and these are applied. v0.3’s stop condition lists round 3 completion as a stop, so confirm whether Status should instead read as stopped and awaiting independent audit.

3. Gap Map. B10 is an incremental recount from the v0.3 baseline. A from-scratch recount is due at audit. v0.5 extends the same incremental recount.

4. Citation carry-over. All source citations, including the new D-UKSC paragraph numbers, are unverified in this fusion (I2 item 5).

5. The [M] tag. The amendment file lists [M] among its tags, but A3 does not define it and v0.4 does not use it. The one sentence the amendment tagged [M] (that it does not re-verify v0.3 citations) is carried as [R] (I2 item 5; K5). Define [M] or confirm its removal.

6. “MSMD”. The K2 row for #19 uses “MSMD” without an expansion in any source file. The A4 glossary gives “minimum safe manning document” as a [S] assumption. Confirm.

7. K2 document locations. The section numbers (for example “Approval basis §2.7”, “ConOps §4.3”) are carried from the amendment file and are unverified navigation aids.

8. S-5 specification gaps. K4 records gaps found at fusion (for example, an approaching vessel already aligned and closing without a detectable course adjustment). Decide whether to resolve them before the audit.

9. S5.6 reference. “ENC accuracy per IHO S-44” is carried from the amendment file. As far as this fusion knows, S-44 is the IHO hydrographic survey standard rather than an ENC product specification. Verify the intended reference. Resolved in v0.5.1 (VR-06): the doubt was correct; S-44 is the IHO Standards for Hydrographic Surveys (Edition 6.1.0, October 2022).

10. Retirement. The Architect directs retirement of v0.3 and the amendment file once v0.4 is built. Their SHA-256 hashes are in J2 and J7 so any archived copy can be matched later. v0.3 J6 item 5 (keep v0.1 and v0.2 as reference copies until the fresh-context audit confirms nothing in J4 or J5 was mishandled) still stands for those two files.

11. Round status. The MRB’s own rule says a round beyond round 3 needs Architect direction or a newly declared question. v0.5 was built on the Architect’s instruction as a source-extension build, not an audit round, and the purpose and τ are unchanged. Confirm whether to record it as round 4, as “3 of 3 plus extension”, or as a new version series.

12. Rungs for [D-GAO]. B9 proposes Rung 4 for GAO’s own findings and Rung 3 for statements GAO attributes to officials or stakeholders. SG rung definitions were not re-read in this build. Confirm.

13. U.S.-centred evidence. GAO-24 is the only supplied source describing a national Administration’s practice in detail, and it is U.S. Decide whether to survey other flag states before audit (GTL-15, GTL-21).

14. Dated GAO evidence. GAO-24 predates the MASS Code by about two years; U.S. statutes and Coast Guard positions may have changed (GTL-17, GTL-20). Decide whether to refresh before external submission.

15. Military analogy scope. Part L, S-7 and F6 use Navy programme findings by analogy, and the MASS Code excludes warships (A2 item 5). Decide whether to keep them in the main bridge or move them to an appendix for external peer review.

16. v0.4 retirement. The Architect directs retirement of v0.4 once v0.5 is built. Its SHA-256 is in J2 and J8, so an archived copy can be matched later.

17. Verification standard. Part M uses public web sources and one primary Coast Guard document, read by the producing session. v0.5.1 narrows or corrects items and closes none of the GTL items. Decide whether web-source checks may ever close a GTL item or only narrow it. Applied in v0.6 through the M5 standard: primary or official text closes, secondary sources only narrow. Pending your confirmation (item 21).

18. Adoption day. v0.4 text says the MASS Code was adopted on 21 May 2026; several summaries say 22 May, and the session ran 13–22 May. Confirm from the resolution’s date stamp before changing A2 item 2 (GTL-01). RESOLVED in v0.6 (VR-15): the resolution text says 21 May 2026, so A2 item 2 stands.

19. Verification queue. Confirm the order in M3 before round 2. Superseded in v0.6 by M3 and M5.

20. Canadian distinct-signal point. GAO-24 reports it, but the policy excerpts read in round 1b did not show it. Keep the GAO-based wording in #5 only with the verification note until the policy text is read.

21. Closure standard. M5 sets how ledger items close. Confirm it, or state a different standard, before the audit.

22. Reclassification requests. (a) Downgrade GTL-03, GTL-04 and GTL-05 (Status Book counts) from verification items to hygiene checks, since they are labelled as Status Book counts and nothing in the bridge relies on them legally. (b) Accept GTL-09 to GTL-12, GTL-14 and GTL-16 as OPEN-EXTERNAL declared limits. (c) Accept GTL-02 as a tracking item (T-1).

### J7. v0.4 LINEAGE RECORD

**Lineage.** v0.1 (round 1) → v0.2 (audit and red-team corrections) → v0.3 (consolidation of v0.1 and v0.2) → v0.4 (fusion of v0.3 with the Round 3 amendment file). Per the amendment’s fusion instructions, all existing IDs were kept unchanged (#1–#28, S-1–S-5, G-1–G-15, BR-01–BR-07, C-01–C-14, GTL-01–GTL-16, RT-01–RT-10). [R]

**Source files fused (as uploaded).** v0.3: `THE_MASS_REGULATORY_BRIDGE_v0_3.md`, 84,075 bytes, SHA-256 `41d8f6278e162c2a9640bf41a4451318a49203e0348c2d6e3cd38c89184a0205`. Amendment: `MRB_v0_4_AMENDMENT.md`, 43,049 bytes, SHA-256 `0e554d608745d083ac426861b59bcbf091d6d525c1dd003b8d0ec5048fa4e7c3`. [R]

**Amendments applied.** RT-01 (C4 #25; GTL-08) · RT-02 (C4 #28) · RT-03 (C5 S-5; K4) · RT-04 (Part E) · RT-05 (B2; BR-02; A2 item 7) · RT-06 (Part K) · RT-07 (#7, #8) · RT-08 (#5) · RT-09 (F5) · RT-10 (B3) · Insight A (K1) · Insight B (K1; S-5) · Insight C (A2 item 7) · Insight D (#28) · GTL statuses (Part H) · τ self-check additions (Part I) · Build State (A1) · Part J lineage (this section). Section G3 gives the RT table. [R]

**Also changed.** C0 index (rows #28 and S-5; #25 status) · A3 source register (D-UKSC) · A4 glossary (ABIL, UKSC, ENC, MSMD) · B9 closure markers extended to D-UKSC · B10 Gap Map recounted · front matter, document map, A1, I1–I3, J1–J2 updated for v0.4 · all “v0.3” self-references in live text moved to “v0.4”. [R]

**Fusion reconciliations (not instructed by the amendment file).** Each reconciles an amendment statement with v0.3’s authority rules (A2: the MASS Code is guidance, COLREG/SOLAS/MARPOL are the mandatory baseline) or with a stated limit, or fixes an internal inconsistency. Revert any of them by Architect direction. [R]

| ID | Where | Reconciliation |
| --- | --- | --- |
| R-1 | Front matter; J6 | v0.4 dated 10 November 2026 (build date); the amendment’s 11 November audit date is recorded, not adopted. |
| R-2 | J6; K5 | Amendment tag [M] is undefined in A3 and is not used; its single use is retagged [R]. |
| R-3 | C5 S-5; K3; K4 | “Mandatory ANS design requirement” and similar “must” wording becomes “proposed”, “should” or “recommended”, because this document is private guidance and cannot create obligations. |
| R-4 | K1; C5 S-5 | Insight B scoped: authoritative in UK law, persuasive elsewhere. Universal negatives (“no IMO guidance, circular or class rule provides this”) become “none identified in the supplied sources”, with flag-state practice unsurveyed (GTL-15). |
| R-5 | A2 item 7; B2 | “COLREG frozen” becomes “practically frozen” (no scheduled amendment, Art. VI still available); “6-year window” becomes “about five years” (to 1 January 2032). |
| R-6 | Part E | RT-04’s “legal equivalence standard” becomes “the equivalence standard the Code applies to evaluation”, plus a note that equivalence arguments are accepted by the Administration and do not amend legacy text. |
| R-7 | K1 | ABIL binding force derives from Administration approval and national implementation during the transition, not from the non-mandatory Code alone. The SOLAS I/5 comparison is tagged [S/GTL]. Interpretation within COLREG’s text is distinguished from a legal deviation. |
| R-8 | K4 | UKSC Groups 1–3 are mapped to states S1–S3; S2 is identified as an engineering buffer [S]; S5.4 specification gaps are listed; S5.7 actions are tagged [S]; the IHO S-44 reference is flagged. |
| R-9 | Part H (GTL-06); C1 #9 | GTL-06’s expanded Rule list rests on UKSC- and HET-quoted text, not the consolidated COLREG. #9’s Rule 19 specific obligations stay [S/GTL] because nothing in the amendment changed that tag. |
| R-10 | B2; BR-02 | RT-05’s stage labels are aligned: the four stages are proposal and circulation; MSC adoption; Assembly adoption and communication to Contracting Parties; entry into force absent objection by more than one-third. |
| R-11 | F5 | “Flag states should require ROC redundancy or limit k_cap” becomes a proposal [S] consistent with F4 and J5 item 11. |
| R-12 | #25; C0; C5 heading; A1 | #25’s “until verified” resolution wording removed; counts updated to 28 core and 5 supplemental rows. |
| R-13 | #25 | “The exact scenario a MASS will face” becomes “a scenario a MASS can face”. |
| R-14 | B10; Part I | Gap Map recounted incrementally, and Part I rewritten for v0.4. |
| R-15 | B9 | Closure markers (anti-hegemonic check, source deception risk, rungs, token presence, supersession) extended to D-UKSC and v0.4. |

### J8. v0.5 LINEAGE RECORD

**Lineage.** v0.1 (round 1) → v0.2 (audit and red-team corrections) → v0.3 (consolidation) → v0.4 (fusion with the Round 3 amendment file) → v0.5 (fusion of v0.4 with three GAO reports). All existing IDs were kept unchanged (#1–#28, S-1–S-5, G-1–G-15, BR-01–BR-07, C-01–C-14, GTL-01–GTL-16, RT-01–RT-10). New IDs: #29, #30, S-6 to S-8, G-16 to G-20, GTL-17 to GTL-22, GF-01 to GF-16. [R]

**Source files fused (as uploaded).** v0.4: `MASS_REGULATORY_BRIDGE_v0_4.md`, 147,480 bytes, 1,357 lines, SHA-256 `7cfaba801c33765c35179af87af3f29687b2878b576fd5c062eebd7fc8bc5fd4`. GAO PDFs and hashes are in J2. [R]

**Changed in v0.5.** Front matter, document map, A1 to A4, B2, B3, B5, B9, B10 (recount), C0 index, addenda labelled “GAO fusion (v0.5)” in #1, #5, #6, #10, #17, #19, #25, #26, new rows #29, #30 and S-6 to S-8, addenda in G-1, G-3, G-5, G-7 to G-10, new gaps G-16 to G-20, F3 item 8, F5 note, F6, G4, Part H (GTL-02, GTL-15 annotated; GTL-17 to GTL-22), Part I, J1, J2, J5, J6, J8, K1 note, K2 rows, K3 bullets, K5 items, Part L. Text not listed here is carried from v0.4 unchanged except for “v0.4” self-references in live text moved to “v0.5” or “v0.4 or v0.5”. [R]

**Fusion rules (v0.5).** (1) GAO findings are paraphrased and cited by page; statements GAO attributes to officials or stakeholders are tagged as reported. (2) Military-programme evidence is used by analogy only. (3) No new claim about the MASS Code or IMO documents is made beyond the supplied sources. (4) Every addition is labelled so it can be reverted. [R]

| ID | Where | Reconciliation |
| --- | --- | --- |
| R-16 | A2 item 3 | GAO-24’s 2025 non-mandatory target against the May 2026 adoption in D-MSC is recorded as a delay, not a conflict. |
| R-17 | #29; G-16 | “Cannot waive” is the Coast Guard’s position as reported by GAO, not a checked statement of statute. |
| R-18 | F6 | The HET reading is [R]; neither GAO report discusses adversaries. |
| R-19 | B3 | Administration plurality is an inference from one flag state. |
| R-20 | B5 | GAO corroboration is attached to existing SG risk labels; no new risk class is created. |

### J9. v0.5.1 LINEAGE RECORD

**Lineage.** v0.5 (GAO fusion) → v0.5.1 (verification round 1). All existing IDs kept; new IDs are VR-01 to VR-10 and J6 items 17–19. [R]

**Source file.** v0.5: `MASS_REGULATORY_BRIDGE_v0_5.md`, 203,449 bytes, 1,659 lines, SHA-256 `661919c27af1644b5adfd3a40fbae3df03610fcfa9ade1d55dca3a865e6e72e2`. [R]

**Changed in v0.5.1.** Front matter, document map, A1, A2 item 3, A3 (new sources D-IMO, D-USC, D-USCG-WI, D-GAO26T), #29 verification update, G-6 verification update, K1 and L3 verification notes, K4 S5.6 ENC row, J1, J2, J5 (items 30–32), J6 (item 9 resolved; items 17–19), this record, Part H (GTL-01, 02, 17, 18, 20, 22 statuses), I2 items 9 and 13, and new Part M. The B10 Gap Map was not recounted: round 1 changes statuses, not claim-group counts. All other text is carried from v0.5. [R]

### J10. v0.5.2 LINEAGE RECORD

**Lineage.** v0.5.1 (verification round 1) → v0.5.2 (round 1 continued: Canada, UK, U.S. pilot). All existing IDs kept; new IDs are VR-11 to VR-14 and J6 item 20. [R]

**Source file.** v0.5.1: `MASS_REGULATORY_BRIDGE_v0_5_1.md`, 218,885 bytes, 1,734 lines, SHA-256 `e6dc1e96a8c3e262438534fa5edb2ecb46cf77fe279b09ba4308fbc839be45ea`. [R]

**Changed in v0.5.2.** Front matter, document map, A1, A3 (D-TC, D-UKSI), #5, #6, #10, #29 and G-1 verification notes, GTL-17 and GTL-21 statuses and the status note, Part M (VR-11 to VR-14, queue, limits), J1, J2, J5 (item 33), J6 (item 20), this record. B10 was not recounted. All other text is carried from v0.5.1. [R]

### J11. v0.6 LINEAGE RECORD

**Lineage.** v0.5.2 (verification round 1 continued) → v0.6 (verification round 2 and closure dispositions). All existing IDs kept; new IDs are VR-15 to VR-21, T-1, J6 items 21–22 and J5 items 34–37. [R]

**Source file.** v0.5.2: `MASS_REGULATORY_BRIDGE_v0_5_2.md`, 225,404 bytes, 1,757 lines, SHA-256 `fdaa6d138e55580e5a622b9c598c3bb9f534083048779e1513f89fc52836e529`. [R]

**Changed in v0.6.** Front matter, document map, A1, A2 item 7, A3 (D-IMOP, D-DOD, D-NMA), notes under #29, #30 and G-18, the L2 COLREG row, GTL statuses for 01, 02, 07, 13, 15, 17, 18, 19, 20, 21 and 22, the status notes, Part M (heading, VR-15 to VR-21, M3, M4, new M5), Part I item 14, J1, J2, J5, J6, this record. B10 was not recounted. All other text is carried from v0.5.2. [R]

## PART K — APPROVAL BASIS INTERPRETATION LAYER (ABIL) AND S-5 RULE-SWITCHING SPECIFICATION

Reading convention for Part K. “Must” and “should” in K2 to K4 state the bridge’s recommended practice for an approval basis. They are not obligations created by the MASS Code or by this document, which is private analytical guidance (A2). Source: Round 3 amendment RT-06, S-5 specification and Insights A, B. [R]

### K1. CONCEPT DEFINITION

**Insight A — the regulatory interpretation layer as a new maritime concept.** The MASS Code creates something that does not exist in conventional maritime law: a vessel-specific, Administration-approved regulatory interpretation encoded in the approval basis, ConOps and regulatory gap analysis. It is not a flag-state circular, not an IMO interpretation, not a court ruling. It is a contractual-regulatory hybrid that, to the extent the Administration makes it a condition of approval, binds the vessel, the Company, the ROC and the Administration. This bridge names the layer the **Approval Basis Interpretation Layer (ABIL)**. The term is not found in MSC.595(111), and this bridge has not found the layer named elsewhere. [D-MSC Ch. 6, Annex 1, Annex 2; R; S]

**Insight B — the UKSC “shaping to enter” test as a design threshold.** The Ever Smart “shaping to enter” test is the first judicially articulated, sensor-observable trigger for COLREG rule-switching, identified in the supplied sources, that can be implemented directly in autonomous navigation software. It is authoritative in UK law and persuasive elsewhere. No IMO guidance, flag-state circular or classification society rule providing an equivalent trigger was identified in the supplied sources; flag-state and class practice is unsurveyed (GTL-15). This bridge treats UKSC para 145 as a design specification, not merely a legal precedent. It defines: (a) the observable condition (course adjustment toward the starboard entrance); (b) the temporal condition (final approach); (c) the legal consequence (rule switch from crossing to narrow channel). [D-UKSC para 145; R; S; ?]

**Definition.** The ABIL is the vessel-specific, Administration-approved regulatory interpretation encoded in the approval basis, ConOps and regulatory gap analysis. It is the mechanism by which COLREG ambiguities are resolved for autonomous operation without amending COLREG itself. [D-MSC Ch. 6; Annex 1; Annex 2 §8.2; R]

Legal basis:

- MASS Ch. 6 establishes a five-step approval process. The “approval basis” (Annex 1 §1.4, §2.5) is a document submitted by the Submitter and approved by the Administration. It is the vessel-specific basis on which the Administration approves and certifies the vessel. During the transition its binding force derives from the Administration’s approval and national implementation, not from the non-mandatory Code alone (A2). [D-MSC Annex 1; R]
- MASS Annex 2 §8.2 requires the ConOps to identify “possible deviations from the applicable rules and regulations and provides justification of alternative solutions based on risk assessment.” [D-MSC Annex 2 §8.2]
- MASS 5.1.3.4 requires the MASS Record to contain a “regulatory gap analysis.” [D-MSC 5.1.3.4]
- COLREG text is practically frozen for about five years of the 2026–2032 transition (A2 item 7). The ABIL is the primary vehicle for COLREG interpretation during that window. [D-SB; R]

The ABIL is not:

- An IMO interpretation (that requires committee action).
- A flag-state circular (that is general, not vessel-specific).
- An exemption or equivalent arrangement under SOLAS I/5 (those are different mechanisms). [S/GTL; SOLAS operative text not supplied]
- A court ruling (though it may encode court rulings, as with Ever Smart).

The ABIL is:

- A per-vessel, Administration-approved regulatory interpretation.
- Binding on the vessel, the Company, the ROC and the Administration to the extent the Administration makes the approval basis a condition of approval or certification.
- Subject to survey and re-approval upon change (MASS 6.4.2).
- The mechanism by which the “level of safety” equivalence standard (MASS 6.2) is demonstrated.

Reconciliation note (v0.4) [R]: where an ABIL entry interprets COLREG text (for example the S-5 rule-switching trigger), it is an interpretation within the text, not a legal deviation from it. Where an entry would depart from the text, the departure must be justified through Annex 2 §8.2 and remains subject to the mandatory legacy text and the flag state’s own authority to accept it. The S5.10 template uses the Annex 2 §8.2 field name “Deviation” for that reason.

v0.5 note — nearest existing analogue (GF-06) [R]. GAO-24 (pp. 10–11, fn. 16–17) describes how the Coast Guard handles autonomous operations today: local Captains of the Port approve operations and testing case by case, using Policy Letters 22-01 (human-supervised testing), 01-20 (novel uses of the marine environment) and 01-23 (design-basis agreements for equivalents), working directly with each applicant and informing other waterway users. That is a per-project, authority-approved arrangement resembling an ABIL entry in function, but it is port-level practice, not the vessel-wide approval basis that MASS Ch. 6 contemplates. Industry raised concerns about consistency between ports, and headquarters said it was working on a common risk-assessment framework (p. 11). The analogy supports two ABIL points: per-project approvals can be made workable, and consistency across approvers is a recurring weakness (K3). It does not show that any Administration will accept ABIL entries of the kind K2 lists. [D-GAO24 pp. 10–11; R; ?]

v0.5.1 verification update — Coast Guard practice (VR-05, VR-08) [R]. The policy-letter basis in the note above is out of date. CG-CVC Policy Letter 22-01 (Change 1) is cancelled by Coast Guard Work Instruction 5P-WI-002(1), original date 1 June 2026, which was read in full. The Work Instruction is non-binding by its own disclaimer, does not implement the MASS Code, and says the Code does not directly apply to the unmanned maritime systems it covers. It directs Captains of the Port and OCMIs to gather from operators a concept of operations that includes control modes, remote-operator procedures and training evidence, emergency procedures, cyber resilience and a COLREGS compliance statement explaining how lookout, manoeuvrability, navigation and lighting requirements will be met (D.1.a). For inspected vessels it has OCMIs send test proposals to CG-CVC for a national recommendation while keeping final approval authority (E.1), which answers the consistency concern in the earlier note by a different route. This is the closest verified analogue to an ABIL entry: a per-operation ConOps and a stated COLREG-compliance explanation reviewed by a local authority. It is still not a vessel-wide approval basis and says nothing on S-5-type thresholds. Policy Letters 01-20 and 01-23 named in the earlier note were not re-checked. [D-USCG-WI D.1.a, E.1; R]

### K2. ABIL MAPPING TABLE

Each friction point maps to a specific approval-basis entry. The table specifies what should be written, where, and what it resolves. The document-location section numbers are carried from the amendment file and are unverified navigation aids (J6 item 7). [R]

| Friction ID | ABIL entry required | Document location | Content | Resolves | Tag |
| --- | --- | --- | --- | --- | --- |
| #1 | Sensor-to-sense equivalence declaration | Approval basis §2; ConOps §3.3 | Declare sensor suite ↔ COLREG Rule 5 senses mapping; declare degradation modes; declare equivalence argument under MASS 6.2 | Rule 5 “sight and hearing” | [D-MSC 16.4.2, 6.2; R] |
| #2 | Remote-master intervention latency | Approval basis §2.7; ConOps §4.1 | Declare maximum latency from danger detection to master intervention; declare ANS fallback response for the interval | Rule 2 remote authority | [D-MSC 8.4.2, 8.7.4; R] |
| #3 | OE-to-Rule-6 parameter mapping | Approval basis §2; ConOps §4.2 | Map each Rule 6 factor to an OE parameter; declare degraded-state buffers before OE exit | Rule 6 continuous judgment | [D-MSC 8.3.1, 8.3.3; R] |
| #4 | Sensor sufficiency threshold | Approval basis §2.7; ConOps §4.2; V&V plan | Declare minimum sensor confidence threshold below which ANS alerts master and enters degraded state; declare uncertainty floor | Rule 7 “scanty information” | [D-MSC 16.4.2 EP2; R] |
| #5 | Manoeuvre legibility validation | Approval basis §2.7; V&V plan | Declare manoeuvre magnitude and timing criteria for visual/radar legibility to conventional vessels; declare digital signalling for MASS-to-MASS | Rule 8 “readily apparent” | [D-MSC 16.4.3; D-UKSC para 40; R] |
| #6 | Small-MASS rule-set declaration | ConOps §8.1; MASS Record §4 | Declare which COLREG rules apply; declare national small-MASS rules; declare TSS/narrow-channel behaviour | Rules 9–10 small MASS | [D-MSC Res. §3; R] |
| #7 | Rule 17(a)(ii) observation threshold | Approval basis §2.7; ConOps §4.3; V&V plan | Declare CPA/TCPA or equivalent threshold at which ANS concludes give-way vessel is not acting; declare observation algorithm parameters | Rule 17(a)(ii) “becomes apparent” | [D-UKSC paras 60–61; D-MSC Annex 1; R] |
| #8 | Rule 17(b) prediction threshold | Approval basis §2.7; ConOps §4.3; V&V plan | Declare prediction-accuracy requirements; declare false-negative/false-positive thresholds; declare escalation criteria to master | Rule 17(b) “cannot be avoided” | [D-UKSC paras 60–61; D-MSC Annex 1 §2.7; R] |
| #9 | Restricted-visibility sensor mode | ConOps §4.2; OE §8.3.1.2.3 | Declare restricted-visibility mode; declare sensor-fusion equivalent of “detects by radar alone”; declare prohibited manoeuvres | Rule 19 sensor mapping | [D-MSC 8.3.1.2.3; R] |
| #10 | Lights/shapes/signals survey checklist | Approval basis §2; V&V plan; survey checklist | Declare automated activation mechanism for Rule 35 sound signals; declare Part C/D compliance verification method for unmanned vessels | Parts C/D verification | [D-MSC 16.2, 5.1.5; R] |
| #11 | Human-system limitation analysis | Regulatory gap analysis; ConOps §7 | Declare human-system limitations of remote operators and ANS; substitute for “limitations of the crew” | Rule 2 crew limitations | [D-MSC 8.7.2, Annex 2 §8.2; R] |
| #12 | Verification evidence stack | Approval basis; MASS Record | Declare flag-state audit + MASS/ROC certificates + vessel incident data as layered evidence; do not collapse layers | Part F granularity | [D-MSC 5–6; D-HET Part F; R] |
| #13 | Electronic means equivalence | Approval basis §2; ConOps §3.3 | Declare how V/19.2.1.4 and .5 are met by electronic means; declare back-up electronic chart system | SOLAS V/19 bridge assumption | [D-MSC 16.3.3 EP1; R] |
| #14 | SCS response chain | ConOps §4.4; approval basis | Declare human/remote response chain for stability events; declare SCS monitoring as crew substitute | SOLAS II-1 crew action | [D-MSC 19.2.2; R] |
| #15 | Fire response without crew | ConOps §5; V&V plan | Declare automated detection + remote/autonomous extinction + external-responder interface; validate single-compartment fire control | SOLAS II-2 crew firefighting | [D-MSC 20.2.7, 20.2.8; R] |
| #16 | Crewless rescue arrangements | ConOps §5; MASS Record §1.2 | Declare rescue equipment deployable without crew; declare accommodation for rescued persons; declare ROC communication for rescued | SOLAS III/V/33 crew | [D-MSC 21.2.3, 21.2.4; R] |
| #17 | ROC security in SSP | SSP; ConOps §6 | Declare ROC as security target; declare remote operator ISPS participation; declare ROC compromise → isolation/fallback procedure | ISPS ship-only scope | [D-MSC 12.4.1–12.4.3; R] |
| #18 | Quadrilateral responsibility interface | SMS; ROCSMS; approval basis | Declare Company ↔ MASS ↔ ROC ↔ Master interfaces; declare responsibility allocation; declare ROM DoC/RMC if alternative management | ISM triangle → quadrilateral | [D-MSC 5.7, 11.2, 11.3; R] |
| #19 | ROC watchkeeping standard | MSMD; ConOps §7; approval basis | Declare rest-hour records for remote operators; declare workload limits; declare multi-MASS alarm-load assessment; declare STCW-equivalent qualification | STCW sea-service gap | [D-MSC 14.2.1.8–.9, 14.2.2, 14.5.1; R] |
| #20 | MARPOL Annex I compliance checklist | ConOps §8.2; MASS Record §4 | Declare automated oil-discharge monitoring; declare IOPP survey treatment of unmanned machinery spaces; declare logging | Annex I unmanned spaces | [D-MSC 9.10, 24; R] |
| #21 | Sewage applicability declaration | ConOps §4.1; MASS Record §1.2 | Declare zero-person operating periods; declare reception/holding arrangements; declare applicability when persons present | Annex IV person-dependent | [D-MSC 21.2.4, 2.3; R] |
| #22 | Garbage management by mode | ConOps §8.2; MASS Record §4 | Declare garbage-management plan by voyage phase and person-presence mode; declare cargo residue handling | Annex V crew assumption | [D-MSC 22, 9.10; R] |
| #23 | Emissions compliance declaration | ConOps §3.2; approval basis | Declare propulsion type; declare Annex VI compliance method; declare alternative fuel equivalences if applicable | Annex VI machinery gap | [D-MSC 24.2.3; R] |
| #24 | Incident reporting assignment | SMS; ConOps §5; approval basis | Assign reporting duty to master/Company/ROC; declare automated detection; declare communications availability | Protocol I actor gap | [D-MSC 9.10.5, 17, 18; R] |
| #25 | Rule 9/15–17 interpretation declaration | ConOps §8.1; approval basis; regulatory gap analysis | Declare flag/coastal-state interpretation of Rule 9 vs Rules 15–17 interaction; encode UKSC three-phase test if operating in UK or a jurisdiction recognizing it; declare ANS rule-priority logic | Rule 9/15–17 conflict | [D-UKSC para 145; D-MSC Annex 2 §8.2; R] |
| #26 | Responsibility allocation matrix | ConOps §7; task allocation summary; approval basis | Declare Flag State → Company → ROC → Master → ANS chain; declare no-responsibility-gap verification; declare ANS authority limits | Responsibility split | [D-MSC 8.6.2, 8.7, Annex 1 §2.4; R] |
| #27 | Verification layer declaration | Approval basis; MASS Record | Declare four distinct verification layers and their non-substitutability; declare evidence required for each | Verification overlap | [D-SB SOLAS (130); D-MSC 5–6; R] |
| #28 | Bearing-based crossing engagement | Approval basis §2.7; ConOps §4.3; V&V plan | Declare that crossing rules engage on steady bearing, not steady course; declare bearing measurement accuracy; validate with erratic-course scenarios | Rule 15 engagement trigger | [D-UKSC para 111; D-MSC Annex 1 §2.7; R] |
| #29 | Statutory complement declaration | ConOps §7; MASS Record §4; approval basis §1 | Declare the flag state’s statutory minimum complement per mode; declare how statutory roles are met; declare the legal route relied on (statute, pilot authority, exemption, none) | Statutory minimum crew | [D-GAO24 pp. 2, 10, 12; D-MSC 8.7, 14; R] |
| #30 | Compliance-evidence retention | Approval basis; MASS Record; SMS | Declare retention and access arrangements for look-out equivalence evidence, V&V results and data logs so they can be produced to investigation authorities | Evidence for COLREG-compliance disputes | [D-MSC 9.10; D-GAO24 fn. 25; R] |
| S-1 | Load Lines/IS Code compliance mapping | Approval basis §2; ConOps §4.4 | Declare Load Lines and 2008 IS Code compliance; declare SCS integration with stability criteria | Load Lines omission | [D-MSC 19.2.1; R] |
| S-3 | Amendment version lock | Approval basis §1.4; actions register | Declare rule version for each instrument; declare amendment horizon matrix; declare update triggers | Version drift | [D-SB; D-MSC 6.4.2, 8.2.5; R] |
| S-4 | Application gate record | MASS Record §4; approval basis §1 | Record Administration’s application-gate decision; declare which instruments are insufficient; declare which chapters invoked | Scope ambiguity | [D-MSC 2.1, 5.1.3; R] |
| S-5 | Three-phase rule-switching state machine | ConOps §4.3; approval basis §2.7; V&V plan | Encode the K4 state machine; declare sensor requirements; declare transition criteria; validate with channel-entrance scenarios | Rule 9/15 switching | [D-UKSC para 145; D-MSC 16.4.2, 16.4.3; R; S] |
| S-6 | Change-control classification | Approval basis §1.4; ConOps; actions register | Declare which software and parameter changes need re-assessment, which are pre-approved within declared bounds, and the evidence for each | Version lock vs iterative change | [D-MSC 6.4.2, 8.2.5; D-GAO26; R; S] |

S-2 (MARPOL electronic record books; unmanned-barge precedent), S-7 and S-8 are analogy rows and have no ABIL entry. [R]

### K3. ABIL USAGE RECOMMENDATIONS

- **For Submitters.** Every friction point in the Cross-Reference Matrix (Part C) that is “Unresolved” or “Partially resolved” should have a corresponding ABIL entry in the approval basis before final approval (MASS Ch. 6, step 4). The entry should demonstrate equivalence under MASS 6.2.
- **For Administrations.** The approval basis is the Administration’s opportunity to verify that every COLREG/SOLAS/MARPOL friction has a vessel-specific resolution. The K2 table works as a checklist. If an entry is missing, the approval is incomplete against this checklist.
- **For ROCs and Companies.** The ConOps entries in K2 are operationally significant. The SMS/ROCSMS should incorporate them, and remote operators should be trained on the declared thresholds.
- **For surveyors.** The V&V plan entries in K2 define what should be tested. Survey per MASS 5.2.2 should verify that declared thresholds are met.
- **Version control.** The ABIL is version-locked to the approval basis. Any change to the ConOps, OE, software or ROC requires re-assessment per MASS 6.4.2 and 8.2.5. [D-MSC]
- **Change cadence (v0.5).** Software that changes faster than the approval cycle needs a declared change-control classification (S-6). [D-GAO26 Snapshot; R; S]
- **Approval consistency (v0.5).** Administrations may wish to give approvers a common risk-assessment framework; GAO-24 (p. 11) reports the Coast Guard working toward one for its Captains of the Port. [D-GAO24 p. 11; R]
- **Acceptance criteria and schedules (v0.5).** An ABIL entry that declares a threshold should also state its acceptance criterion and when the evidence will exist relative to the approval decision. GAO-22 (pp. 26–28) found Navy prototypes without measurable readiness criteria or integrated schedules, with a risk of concurrency. [D-GAO22 pp. 26–28; R]

### K4. S-5 FORMAL SPECIFICATION: THREE-PHASE RULE-SWITCHING STATE MACHINE (PROPOSED DESIGN RULE)

Status of this specification: a proposed design rule [S]. It is grounded in UKSC para 145 [D-UKSC] but has not been validated by any flag state, classification society or IMO body, and its numeric thresholds are engineering proposals [S].

#### S5.1 Purpose and legal basis

This specification defines proposed ANS logic for determining which COLREG rule set governs a MASS encounter at or near a narrow channel entrance. It implements the UKSC’s “shaping to enter” test ([2021] UKSC 6, para 145) as a sensor-fusion state machine. [D-UKSC; R; S]

Legal authority, UKSC para 145: “The crossing rules are only overridden if and when the approaching vessel is shaping to enter, adjusting her course so as to reach the entrance on her starboard side of it, on her final approach.” [D-UKSC] The judgment is UK law; the ABIL must declare which jurisdiction’s interpretation applies (K5). [R]

MASS Code basis: MASS 16.4.2 (situational awareness: perception, comprehension, projection); MASS 16.4.3 (collision avoidance based on risk assessment); MASS 8.2 (ConOps); MASS Annex 1 §2.7 (V&V plan). [D-MSC]

#### S5.2 State definitions

| State | Name | Definition | Governing rules |
| --- | --- | --- | --- |
| S1 | CROSSING | Approaching vessel is NOT intending to enter the channel, OR is intending but NOT YET shaping | COLREG Rules 15–17 (crossing rules) |
| S2 | TRANSITION | Approaching vessel is adjusting course toward the channel entrance but has not yet committed to final approach | COLREG Rules 15–17 (crossing rules) with enhanced monitoring |
| S3 | SHAPING | Approaching vessel is shaping to enter: adjusting course to reach entrance on starboard side, on final approach | COLREG Rule 9 (narrow channel rules) override crossing rules |

Mapping to the UKSC groups (fusion note, R): Group 1 (crossing, not intending to enter) maps to S1; Group 3 (intending or preparing but not yet shaping, for example waiting for a pilot) maps to S1, or to S2 once a converging course adjustment begins; Group 2 (shaping on final approach) maps to S3. S2 is an engineering buffer state [S] added by this specification. It is not a UKSC category, and its governing rules are the same as S1’s, with enhanced monitoring.

#### S5.3 Observable conditions

Each state is determined by three observable components, all of which must be assessed by the ANS sensor fusion:

| Component | Observable | Sensor requirement |
| --- | --- | --- |
| C1: Course adjustment | Is the approaching vessel adjusting her course? | Bearing rate of change; heading rate; course-over-ground vector change over time window ≥ 60 seconds |
| C2: Target geometry | Is the adjustment directed toward the channel entrance on her starboard side? | Relative position of vessel to channel entrance geometry; channel entrance coordinates from ECDIS/ENC; vessel’s projected course intersection with entrance |
| C3: Final approach | Is the vessel on her final approach (not merely manoeuvring, waiting, or transiting)? | Speed and distance to entrance; rate of closure; absence of holding pattern or station-keeping behaviour; pilot boarding status if available via AIS/VHF |

#### S5.4 State transition logic

```
INITIAL STATE: S1 (CROSSING)

TRANSITION S1 -> S2:
  IF C1 = TRUE (course adjustment detected)
  AND C2 = PARTIAL (adjustment direction converges on entrance but not yet aligned)
  THEN -> S2

TRANSITION S2 -> S3:
  IF C1 = TRUE (sustained course adjustment)
  AND C2 = TRUE (course aligned to reach entrance on starboard side)
  AND C3 = TRUE (final approach confirmed: closing, not holding)
  THEN -> S3

TRANSITION S3 -> S2 (reversion):
  IF C3 = FALSE (vessel aborts final approach, begins holding or manoeuvring away)
  THEN -> S2

TRANSITION S2 -> S1 (reversion):
  IF C1 = FALSE (course adjustment ceases)
  OR C2 = FALSE (adjustment no longer directed at entrance)
  THEN -> S1
```

Specification gaps noted at fusion (not resolved here) [R]:

1. No path covers an approaching vessel that is already aligned with the entrance and closing but shows no detectable course adjustment (C1 = FALSE, C2 = TRUE, C3 = TRUE). As written it would stay in S1. Whether that vessel is “shaping to enter” under para 145 is a design question for the approval basis.
2. There is no direct S1 → S3 path, so a vessel that becomes aligned and closing within one update cycle must pass through S2.
3. The reversion hysteresis (S5.5) applies to reversions only; forward transitions rely on the C1 detection window alone.

#### S5.5 Transition thresholds (to be declared in the approval basis)

The thresholds are vessel-specific and should be declared in the approval basis. The values below are proposed defaults for a 500 GT+ MASS:

| Parameter | Proposed default | Justification | Tag |
| --- | --- | --- | --- |
| C1 detection window | ≥ 60 seconds sustained course change ≥ 5° | Below this, noise; above, genuine manoeuvre | [S] |
| C2 alignment tolerance | Projected course within ±10° of entrance axis | Consistent with Rule 9(a) “as near to the outer limit... as is safe and practicable” | [S] |
| C3 closure rate | Distance to entrance decreasing at ≥ 0.5 knots AND distance ≤ 2 nm | Distinguishes final approach from holding | [S] |
| C3 station-keeping detection | Speed over ground ≤ 1 knot for ≥ 5 minutes OR heading oscillation ±15° without net closure | Identifies Group 3 (waiting) vessels — keeps in S1/S2 | [S] |
| Reversion hysteresis | State must persist ≥ 30 seconds before reversion triggers | Prevents oscillation at boundaries | [S] |

All thresholds are [S] (proposed) and must be validated in V&V per MASS Annex 1 §2.7. They are NOT derived from the UKSC text, which provides the legal test but not numeric values. The Administration may require different values. [R]

#### S5.6 Sensor requirements

| Sensor | Function | Minimum performance |
| --- | --- | --- |
| Radar (X-band or S-band) | Bearing, range, course of approaching vessel | Bearing accuracy ≤ 1°; range accuracy ≤ 1% of range |
| AIS | Vessel identity, position, course, speed, navigational status | Position accuracy ≤ 10 m; update rate ≤ 2 s |
| ECDIS/ENC | Channel entrance geometry, buoy positions | ENC conforming to the IHO ENC product specification (S-57, or S-101 where available), with data-quality (CATZOC) values reviewed; IHO S-44 sets survey standards for the data behind the chart and is not the ENC specification (verified v0.5.1, VR-06) |
| EO/IR camera | Visual aspect confirmation; light/shape observation | Resolution sufficient to identify navigation lights at ≥ 2 nm |
| GNSS | Own-ship position for relative geometry | Accuracy ≤ 5 m |

Minimum-performance values are proposed [S]. Degraded mode: if radar is unavailable, AIS + EO/IR may suffice for C1 and C2 but not C3 (closure rate). If AIS is unavailable, radar + EO/IR suffice. If both radar and AIS are unavailable, the ANS must enter degraded state per MASS 8.4 and alert the master. [D-MSC 8.4; R]

#### S5.7 ANS actions by state (proposed [S])

| State | ANS action | Master/ROC notification |
| --- | --- | --- |
| S1 | Apply crossing rules. If MASS is give-way: execute Rule 16 early and substantial action. If MASS is stand-on: maintain course/speed; monitor for Rule 17(a)(ii) trigger. | Standard watchkeeping alerts |
| S2 | Apply crossing rules with enhanced monitoring. Increase bearing observation frequency. Prepare for possible state transition. Alert master of potential rule change. | Advisory alert: “Approaching vessel may be shaping to enter channel. Monitoring.” |
| S3 | Switch to narrow channel rules. MASS must comply with Rule 9(a) (keep to starboard side). Crossing obligations cease. If MASS is outbound: maintain starboard side; do not expect give-way from entering vessel. If MASS is inbound: shape course to enter on starboard side. | Alarm: “Rule set changed to narrow channel rules. Crossing rules no longer apply.” |

The S3 actions are proposals and should be checked against the Rule 9 text and the UKSC reasoning at audit; the operative Rule 9 text is partly [S/GTL] (GTL-06). [S; GTL]

#### S5.8 Verification and validation requirements

The V&V plan (MASS Annex 1 §2.7) should include:

| Test | Scenario | Pass criterion |
| --- | --- | --- |
| V1 | Vessel crossing channel entrance, NOT intending to enter (Group 1) | ANS remains in S1; crossing rules applied throughout |
| V2 | Vessel shaping to enter on final approach (Group 2) | ANS transitions S1 → S2 → S3; rule switch occurs at correct point |
| V3 | Vessel waiting outside entrance for pilot (Group 3, ALEXANDRA 1 scenario) | ANS remains in S1 or S2; crossing rules continue to apply; NO premature switch to S3 |
| V4 | Vessel begins shaping then aborts (reversion) | ANS transitions S2 → S1 or S3 → S2 correctly |
| V5 | Erratic-course give-way vessel (UKSC para 111 scenario) | Crossing rules engage on steady bearing despite unsteady course |
| V6 | Sensor degradation (radar lost) | ANS enters degraded state; alerts master; does NOT make state transition on insufficient data |
| V7 | Multiple vessels at channel entrance | ANS correctly assigns state per vessel; no cross-contamination |
| V8 | Night operation; lights only | ANS uses EO/IR to confirm aspect; state logic functions without radar |

Tests for the S5.4 specification gaps (an aligned, closing vessel with no detectable course adjustment) are not in the amendment file and are an open addition. [R]

#### S5.9 ConOps declaration template (proposed)

The following text is a proposed template for the ConOps (per MASS Annex 2 §4 and §8.2):

> SECTION [X]: CHANNEL ENTRANCE RULE-SWITCHING LOGIC
>
> This MASS implements the three-phase rule-switching state machine per UKSC [2021] UKSC 6 para 145. The ANS determines the applicable COLREG rule set at channel entrances based on three observable conditions: course adjustment, target geometry, and final approach status.
>
> In State S1 (CROSSING), Rules 15–17 apply.
> In State S2 (TRANSITION), Rules 15–17 apply with enhanced monitoring.
> In State S3 (SHAPING), Rule 9 applies and crossing rules are overridden.
>
> Declared thresholds: [insert vessel-specific values from approval basis].
>
> The state machine reverts if the approaching vessel aborts final approach. The ANS does NOT switch to narrow channel rules for a vessel that is merely “intending and preparing to enter” but not yet shaping (UKSC Group 3).
>
> This logic has been validated per V&V plan tests V1–V8.

The final sentence is true only once V1–V8 have actually been run. [R]

#### S5.10 Regulatory gap analysis entry template (proposed)

The following text is a proposed entry for the regulatory gap analysis (MASS Record §4, per MASS 5.1.3.4 and Annex 2 §8.2):

| Field | Content |
| --- | --- |
| Gap | GAP [X]: COLREG Rule 9 / Rules 15–17 Interaction at Channel Entrances |
| Affected rule | COLREG Rules 9, 15, 16, 17 |
| Nature of gap | COLREG text does not specify the precise trigger for switching between crossing rules and narrow channel rules at channel entrances. The UKSC [2021] UKSC 6 provides a three-phase test (“shaping to enter”) but this is jurisdiction-specific and not encoded in IMO guidance. |
| Deviation | The ANS implements the UKSC three-phase test as a state machine. This is a deviation from a purely text-based COLREG reading because the text alone does not provide the switching trigger. |
| Justification | The UKSC test is the only legally authoritative, sensor-observable trigger identified for this purpose. It is consistent with COLREG’s purpose (safe navigation) and with MASS 6.2 (level of safety expected of a conventional ship). A competent mariner would apply this test. |
| Alternative solutions considered | (1) Always apply narrow channel rules near entrances — rejected: over-broad, contradicts UKSC. (2) Always apply crossing rules — rejected: contradicts Rule 9. (3) Flag-state-specific rule — adopted: declared in ConOps. |
| Risk assessment reference | [Link to risk assessment per MASS Ch. 7] |

Fusion note (R): “only legally authoritative” in the amendment file is scoped here to “identified”, consistent with K1 Insight B; the template’s “Deviation” field follows the Annex 2 §8.2 wording (see the K1 reconciliation note).

### K5. DECLARED LIMITS OF PART K AND THE ROUND 3 AMENDMENTS

1. The three-phase state machine (S-5) is a proposed design rule [S]. It has not been validated by any flag state, classification society or IMO body. It is grounded in the UKSC judgment [D-UKSC], but the numeric thresholds are engineering proposals [S].
2. The ABIL concept is this bridge’s naming of a mechanism that exists implicitly in the MASS Code. The term “ABIL” is not found in MSC.595(111). [R; S]
3. The “no steady course” finding (#28) is directly from the UKSC [D-UKSC]; its implications for ANS sensor architecture are derived [R].
4. All thresholds in S5.5 are proposed defaults [S] and require V&V.
5. The COLREG freeze window (A2 item 7) is derived from Status Book data [D-SB] and the MSC roadmap [D-MSC Annex 17]. It is a practical, not a legal, freeze and could change if an extraordinary COLREG amendment cycle is convened. [R; ?]
6. v0.4 and v0.5 do not re-verify v0.3 or amendment-file citations (I2 item 5). They are assumed correct pending the fresh-context audit. [R]
7. The UKSC judgment is UK law. It is persuasive but not binding in other jurisdictions. The ABIL must declare which jurisdiction’s interpretation applies. [D-UKSC; R]

8. v0.5: GAO-24 (p. 13) reports that the Coast Guard saw how autonomous technology complies with collision regulations as not yet established. That is consistent with there being no equivalent of S-5 in U.S. practice as of mid-2024, but it is not evidence about other flag states or the MASS Code, and GAO-24 does not mention the UKSC test. [D-GAO24 p. 13; R]

9. v0.5: the comparison with Coast Guard practice (K1 note) is an analogy. No Administration has been shown to accept the ABIL entries in K2. [R; ?]

## PART L — GAO FUSION: EVIDENCE AND STRUCTURAL ANALOGUES (v0.5)

Reading convention for Part L. Part L collects what the three GAO reports add, what they do not support, and where this bridge uses military-programme findings by analogy. GAO findings are paraphrased and cited by printed page (GAO-22, GAO-24), letter page or Snapshot (GAO-26). [R]

### L1. SOURCE CHARACTERIZATION AND LIMITS

| Source | Date | Subject | Supports in this bridge | Does not support |
| --- | --- | --- | --- | --- |
| GAO-22-104567 | 7 April 2022 | U.S. Navy uncrewed maritime systems: cost, management, prototyping | G-8 scale; G-19; F6; S-7; K3; analogue for #26 | Commercial regulation; any COLREG, SOLAS or MARPOL content; Navy figures are dated |
| GAO-24-107059 | 8 August 2024 | Commercial autonomous ships; IMO process; Coast Guard regulation; Canada, Norway, UK | #29, #30; A2 items 3, 7, 8; B2, B3; #1, #5, #6, #19; G-16 to G-18; GTL-17 to GTL-21 | The MASS Code (it predates it); non-U.S. flag-state depth; the UKSC test, ABIL or S-5 (not mentioned); officials’ statements are second-hand |
| GAO-26-109014 | 15 June 2026 | Navy RAS leadership and organization | S-6; F6; L4; G-8 | Commercial regulation; classified detail (omitted); March 2025 findings partly overtaken by later changes |

### L2. WHAT THE GAO EVIDENCE DOES TO v0.4 CLAIMS

| v0.4 claim | Effect | Note |
| --- | --- | --- |
| COLREG practically frozen 2026–2032 (A2 item 7) | Corroborated for amendment cadence; qualified for the scoping outcome | GAO-24 reports an IMO no-amendment position in 2024 (second-hand). MSC.1/Circ.1638 Table 3 lists COLREG as high-priority with option II (amend) for degree four, so “no amendment” is a later decision not yet traced to the MSC record (VR-16) |
| Roadmap target 2032 (A2 item 3) | Corroborated | Same year in GAO-24 p. 7; non-mandatory step came later than the 2025 expectation |
| ABIL as the main interpretation vehicle (K1) | Not tested; analogue found | Captain of the Port practice (K1 note, L3) |
| S-5 UKSC three-phase test | Not tested | GAO-24 is silent on the UKSC; U.S. compliance method “not established” |
| #1 look-out equivalence | Extended | Evidence base absent (G-17) |
| #19, G-7 ROC watchkeeping | Extended | Remote operators as seafarers; masters over several ships |
| #6, G-1 small MASS | Extended in part | Canada, UK measures; U.S. case-by-case |
| F5 k_cap | Extended | Master-level count added |
| A2 authority rule (domestic law is the mandatory baseline) | Extended | Domestic statutes mapped (#29) |
| Insight B “none identified in the supplied sources” | Not contradicted | See K5 item 8 |
| HET hidden centralization (F2) | Extended by analogy | F6 |

### L3. U.S. ADMINISTRATION PRACTICE AS A WORKED EXAMPLE

GAO-24 (pp. 10–14, Table 1) reports that the Coast Guard says existing laws suffice for its safety mission; applies current regulations case by case through local Captains of the Port; has issued no autonomous-specific regulation since 1987–88; allows automated systems to replace some engineering crew on evidence of capability, reliability and maintenance; grants equivalents; supports human-supervised testing under Policy Letter 22-01; chartered AutoPoCo on 22 June 2021; issued a 2020 request for information; and will develop policy guidance and design standards when the technology reaches critical mass, saying the conditions for rulemaking had not been reached. It also reports that the Coast Guard does not currently plan to amend regulations or issue guidance before the IMO framework. [D-GAO24 pp. 10–14; R]

Observations [R]: (1) the U.S. posture is to wait for the IMO framework and critical mass, which fits the practical freeze; (2) per-project approvals are resource-intensive, as one Captain of the Port said (pp. 10–11); (3) statutes bound the outcome, so case-by-case approval cannot reach below statutory minimums (#29); (4) one pilot-programme participant raised the slow pace of policy guidance (p. 11). For a Submitter: do not assume an ABIL entry can go below statutory minimums, and plan for case-by-case review.

v0.5.1 verification note (VR-05). The Policy Letter 22-01 reference above is superseded; see the K1 verification update. The Coast Guard position that it cannot waive statutory crew minimums was still stated in December 2025 (GAO-26-108762, excerpts), and the Work Instruction of 1 June 2026 sets manning no lower than the statutory minimum. Whether AutoPoCo and the 2020 request for information still exist in the same form was not checked. [D-USCG-WI; D-GAO26T; ?]

### L4. STRUCTURAL ANALOGUE: NAVY RAS PROGRAMME AND THE IMO INSTRUMENT STACK

| GAO finding | Navy context | Analogue in this bridge | Strength |
| --- | --- | --- | --- |
| Domain- and platform-siloed organization leaves common enablers underfunded (GAO-22 pp. 20, 23; GAO-26 Snapshot) | Three offices split uncrewed funding; digital infrastructure got a small share of spending | Instrument-by-instrument cycles with no owner of the cross-instrument seam (B2, B6); the ABIL handles the seam per vessel | Medium |
| No empowered integrating authority (GAO-22 pp. 21–22; GAO-26 p. 2 fn. 5) | No single leader; a portfolio acquisition executive created in 2025 | Responsibility chain (#26); K3 | Medium |
| Early fixed requirements versus iterative development (GAO-26 Snapshot) | Long acquisition timelines for LUSV and XLUUV | S-6 | Low to medium |
| No measurable readiness criteria for prototypes (GAO-22 pp. 26–27) | Prototypes moved on without criteria | #3, #4, #7; K3 acceptance criteria | Medium |
| Crew checks becoming software checks (GAO-22 p. 33) | Certification conversion | S-7 | Medium |
| Crew numbers and sustainment cost unknown (GAO-22 p. 16) | Optimal-manning history | G-19 | Low to medium |
| Common enabling architecture (GAO-22 pp. 3, 30; GAO-26 Snapshot) | Shared autonomy architecture and lab | F6 | Medium |

Limits. Navy acquisition and budgeting differ from international regulation. GAO’s recommendations (portfolio management, stakeholder roles) are addressed to the Navy and are not proposals for IMO. The Navy’s concurrence and later actions (GAO-22 pp. 35–37; GAO-26 letter pp. 2–3) are not evidence that those actions work. [D-GAO22; D-GAO26; R]

### L5. DECLARED LIMITS OF PART L

1. The evidence is U.S.-centred and weighted to one audit body (B9). [R]
2. The evidence is dated (I2 item 10). [?]
3. Statements attributed to officials and stakeholders are second-hand; stakeholder counts follow GAO’s quantifier convention (A3). [D-GAO24 p. 15]
4. Analogues are analogies, not findings about commercial MASS. [R]
5. Navy dollar and fleet figures are used only as dated illustration. [R]
6. Statutes, cases, policy letters and IMO documents cited by GAO were not checked (GTL-17 to GTL-22). [?]
7. Part L adds no new SG read; the B-part labels are unchanged. [R]

## PART M — VERIFICATION LOG (ROUNDS 1–2, v0.6)

### M1. METHOD AND LIMITS

Round 1 checked items that could be settled from public sources: IMO web pages, the text of 46 U.S.C. § 8301, the Coast Guard Work Instruction named in a search result (fetched and read in full), IHO standards pages, and excerpts of a GAO testimony. The producing session did the checking, so this is not an independent audit (D-BP §V1). Web summaries are not the instruments themselves. Each record states what was checked, the result, and what is still open. Results use these words: CONFIRMED, PARTIAL, CORRECTED, RESOLVED, CLOSED. Round 2 added a closure standard (M5). [R]

### M2. RECORDS

| ID | Item | Result | Open remainder | Effect on the document |
| --- | --- | --- | --- | --- |
| VR-01 | GTL-01 MASS Code adoption, effect date, non-mandatory status, MASS under 500 GT | CONFIRMED: MSC.595(111), MSC 111 (13–22 May 2026), effect 1 July 2026, non-mandatory, invitation for MASS under 500 GT, all on IMO pages [D-IMO] | Adoption day: 21 May (v0.4 text) against 22 May (several summaries); needs the resolution date stamp | GTL-01 annotated; J6 item 18 |
| VR-02 | GTL-02 2032 roadmap | CONFIRMED with qualification: IMO-side summaries say 1 January 2032 at the earliest, may be revisited; MSC 112 (December 2026) to re-establish the MASS working group for the experience-building phase [D-IMO] | Annex 17 not re-read; class-society summary gives a 2030 adoption target | A2 item 3; GTL-02 |
| VR-03 | GTL-17 U.S. statutes and no-waiver position | PARTIAL: § 8301 read; scope is inspected vessels with exceptions; emergency suspension in (d); no-waiver position repeated December 2025 (excerpts); Work Instruction sets manning no lower than § 8301 and Part 15 minimums | §§ 8101, 8102, 8103, 8502, 4312, 10101; pilot status; other flag states | #29 verification update; GTL-17; J5 item 32 |
| VR-04 | GTL-18 IMO look-out position | PARTIAL: scoping outcome identified as MSC.1/Circ.1638 (3 June 2021); secondary sources summarise it as keeping COLREG as the reference point, and commentators differ on whether it flagged amendment needs | Circular text on Rule 5 not read | GTL-18; A2 item 7 wording (“as reported”) kept |
| VR-05 | GTL-20 Coast Guard policy letters | CORRECTED: Policy Letter 22-01 (Change 1) is cancelled by Work Instruction 5P-WI-002(1) of 1 June 2026, read in full. The Work Instruction asks operators for a ConOps and a COLREGS compliance statement, and routes inspected-vessel test proposals through CG-CVC | Policy Letters 01-20 and 01-23; Marine Safety Manual Vol. III; 46 C.F.R. §§ 15.715, 62.50-30 | K1 and L3 notes; GTL-20; J5 item 30 |
| VR-06 | J6 item 9 IHO S-44 | RESOLVED: S-44 is the IHO Standards for Hydrographic Surveys (Edition 6.1.0, October 2022); the ENC product specification is S-57, with S-101 as the next generation | None | K4 S5.6; J6 item 9; J5 item 31 |
| VR-07 | GTL-22 FY2026 NDAA changes | PARTIAL: Pub. L. 119-60 signed 18 December 2025; 10 U.S.C. § 1732 added by § 1802(a); § 811 repeals many earlier provisions | Repeal of § 218 of the FY2021 NDAA by § 811(b) rests on GAO-26 only | GTL-22 |
| VR-08 | New evidence from the Work Instruction | RECORDED: for inspected vessels OCMIs may not set manning below statute; CG-CVC may consider reducing below guideline manning; scope excludes public vessels and small NOAA systems; the Code is acknowledged but not implemented | Work Instruction is non-binding by its own disclaimer | #29; K1 |
| VR-09 | GAO refresh of GAO-24 | IDENTIFIED: GAO-26-108762 (December 2025 testimony) repeats the Coast Guard no-waiver and no-amendment-ahead-of-IMO positions | Read only through excerpts | A3 (D-GAO26T); #29 |
| VR-10 | MARPOL side of G-6 | RECORDED: IMO reports that PPR is tasked with scoping and gap analysis of MEPC instruments, that LEG has a road map, and that FAL is assessing the Code | No output from these processes found | G-6 |
| VR-11 | GTL-21 Canada | CONFIRMED in excerpts: Tier I Policy TP 13585, effective 1 February 2022; degree three or four; 12 m or less or 15 gross tons or less; no crew or passengers aboard; Marine Technical Review Board route; very small craft exempt under conditions; a separate Tier I policy on autonomous navigation systems exists [D-TC] | GAO-24’s distinct-signal and prior-notice points were not seen in the excerpts; annexes and the second policy not read | #5, #6 |
| VR-12 | GTL-21 UK | CONFIRMED in excerpts: SI 2023/1216 in force 13 December 2023; remotely operated unmanned vessel defined; under 24 m; log book kept at the remote operation centre [D-UKSI]. Annex 2 points (single-failure rule at the centre, not-under-command signals on lost link, several vessels per remote operator case by case) come from a law-firm summary only | Annex 2 text not read | #6, #10, F5, G-7 |
| VR-13 | GTL-17 pilot basis | PARTIAL: § 11504 pilot is set out as a note to 14 U.S.C. § 501; GAO-26-108762 says it gives authority to waive certain crew requirements | Pilot text, duration and status not read | #29 |
| VR-14 | U.S. small uncrewed systems leads | LEAD: Coast Guard Authorization Act of 2025 versions include a small-uncrewed-systems pilot and a NOAA seat on AutoPoCo; FY2026 NDAA § 7331 defines NOAA small unmanned systems (35 feet or less), cited in the Work Instruction | Enactment and final text not checked | G-1 |
| VR-15 | GTL-01 adoption date | CLOSED: the official resolution text on imo.org carries “adopted on 21 May 2026” (Annex 16 to MSC 111/22/Add.1); summaries giving 22 May reflect the session’s closing day [D-IMOP] | None | GTL-01; J6 item 18 resolved |
| VR-16 | GTL-18 IMO scoping outcome on COLREG | CORRECTED: MSC.1/Circ.1638 read through annex page 66; § 6.7 and Table 3 class COLREG as high-priority with option I (degree one), I–II (degrees two and three) and II (degree four). The “no amendment” position GAO-24 reports is a later decision [D-IMOP] | COLREG appendix of the Circular and the MSC 108–111 records not read | A2 item 7; L2; GTL-18; J5 item 34 |
| VR-17 | GTL-07 Rule 28 | CLOSED: 33 C.F.R. § 83.28 is [Reserved] in eCFR-derived tables (2024, 2025 listings); Rule 28 applies in international waters only | None | GTL-07 |
| VR-18 | GTL-13 glider seizure | CLOSED: 15 December 2016, about 50 nautical miles northwest of Subic Bay, USNS Bowditch; PLA Navy vessel 510; returned 19 December 2016 [D-DOD] | None | GTL-13 |
| VR-19 | GTL-19 Pennsylvania Rule | CLOSED for the doctrine; stricter original wording and softer later formulations recorded. Application to autonomous vessels is for counsel | Havinga not checked; application OPEN-COUNSEL (G-18) | #30; G-18; GTL-19; J5 item 35 |
| VR-20 | GTL-21 Norway | CONFIRMED: NMA circular RSV 12-2020 of 27 August 2020 (autonomy levels 3–5, domestic voyages, IMO equivalence process); Yara Birkeland operating with three crew per NMA material [D-NMA] | Yara’s hoped-for crew of two and the circular’s planned revision not confirmed | GTL-21 |
| VR-21 | GTL-17 further statute text | PARTIAL: 46 U.S.C. § 8103(a) text confirmed (documented vessels); § 8101 and § 8102 headings confirmed | Text of §§ 8101, 8102, 8502, 4312, 10101 not read | #29; GTL-17 |

### M3. REMAINING QUEUE (AFTER ROUND 2)

Open-doable items, in order (each can be finished from public primary text):

1. GTL-18: read the COLREG entry in MSC.1/Circ.1638 Appendix 2 and agenda item 5 of the MSC 108 to 111 reports to trace the “no amendment” decision.
2. GTL-17: read the text of §§ 8101, 8102, 8502, 4312 and 10101 and the pilot text; check for changes after December 2025.
3. GTL-20: Policy Letters 01-20 and 01-23, Marine Safety Manual Vol. III, 46 C.F.R. §§ 15.715 and 62.50-30.
4. GTL-22: § 811(b) of Pub. L. 119-60.
5. GTL-06: compare the COLREG text the bridge quotes (Rules 1, 10, 20–37, 39–41 first) with the Coast Guard Navigation Center amalgamation of the consolidated COLREG.

Items that need the Architect’s own files or outside work are listed as open-external in M5. [R]

### M4. DECLARED LIMITS OF PART M

1. Round 2 closed GTL-01, GTL-07, GTL-13 and the doctrinal part of GTL-19 against primary or official sources; earlier rounds narrowed or corrected seven items and resolved one J6 item. [R]
2. Web summaries, a class-society page and trade articles were used as corroboration only where marked. [R]
3. The Coast Guard Work Instruction was read in full; GAO-26-108762 was seen only in excerpts. [R]
4. The Gap Map (B10) was not recounted. [R]
5. A fresh-context audit is still required. [D-BP §V1]

### M5. CLOSURE STANDARD AND LEDGER DISPOSITIONS

**Standard (applied in v0.6; J6 item 21 asks the Architect to confirm).** A ledger item is CLOSED-VERIFIED when the claim was checked against primary or official text and the result is recorded. It is CLOSED-RESCOPED when the claim was narrowed or corrected, the verified part is recorded, and any residual is moved to a named open item or a tracking item. It is OPEN-DOABLE when public primary text can settle it and the reading has not been done. It is OPEN-EXTERNAL when settling it needs the Architect’s source files, outside work, a future event, or a protocol run. A document is ready for audit when no OPEN-DOABLE item remains; OPEN-EXTERNAL items stay as declared limits. Secondary sources can narrow an item but do not close it. [R]

| GTL | Disposition | Residual, owner or trigger |
| --- | --- | --- |
| GTL-01 | CLOSED-VERIFIED | None |
| GTL-02 | CLOSED-RESCOPED | Tracking item T-1: MSC 112 (December 2026) and SOLAS XVI text |
| GTL-03 | OPEN-EXTERNAL | Needs the Status Book or IMO treaty database; Architect may downgrade to hygiene (J6 item 22) |
| GTL-04 | OPEN-EXTERNAL | Same as GTL-03 |
| GTL-05 | OPEN-EXTERNAL | Same as GTL-03 |
| GTL-06 | OPEN-DOABLE | Queue item 5 |
| GTL-07 | CLOSED-VERIFIED | None |
| GTL-08 | CLOSED-VERIFIED | Closed in Round 3 audit; carried |
| GTL-09 | OPEN-EXTERNAL | Needs consolidated SOLAS text (Architect’s copy) |
| GTL-10 | OPEN-EXTERNAL | Needs STCW Convention and Code text |
| GTL-11 | OPEN-EXTERNAL | Needs Load Lines and IS Code text |
| GTL-12 | OPEN-EXTERNAL | Needs consolidated MARPOL annexes |
| GTL-13 | CLOSED-VERIFIED | None |
| GTL-14 | OPEN-EXTERNAL | HET protocol run |
| GTL-15 | CLOSED-RESCOPED | Other-flag-state survey moves to G-1 (OPEN-EXTERNAL) |
| GTL-16 | OPEN-EXTERNAL | Needs an actual ROC architecture and a red-team exercise |
| GTL-17 | OPEN-DOABLE | Queue item 2 |
| GTL-18 | OPEN-DOABLE | Queue item 1 |
| GTL-19 | CLOSED-VERIFIED | Doctrine closed; application is OPEN-COUNSEL under G-18 |
| GTL-20 | OPEN-DOABLE | Queue item 3 |
| GTL-21 | CLOSED-RESCOPED | Three low-materiality residual points under #5, #10, #19 |
| GTL-22 | OPEN-DOABLE | Queue item 4 |

Tally: 5 closed-verified (GTL-01, 07, 08, 13, 19), 3 closed-rescoped (GTL-02, 15, 21), 5 open-doable (GTL-06, 17, 18, 20, 22), 9 open-external (GTL-03, 04, 05, 09, 10, 11, 12, 14, 16); 5 + 3 + 5 + 9 = 22. [R]

---

END OF DOCUMENT — THE MASS REGULATORY BRIDGE v0.6

Produced for Architect Sheldon K. Salmon. This document is not an IMO instrument, not legal advice, not a flag-state circular, and not a certification basis. It is a private analytical document for structural regulatory harmonization, and it has not been independently audited.
