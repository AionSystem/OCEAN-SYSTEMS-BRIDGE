Ocean Systems Bridge (OSB)
A working architecture for managing regulatory, scientific, and operational friction across ocean domains where no single community has the whole picture.

This repository is a documentary workspace and evolving file structure, not an application build. Its purpose is to organize source material, domain maps, specifications, and future build requirements so they can be developed and reviewed separately.

What OSB is
Ocean Systems Bridge is a proposed layered framework for turning regulatory text, unsettled science, and competing institutional interests into declared, bounded, testable, and auditable claims. The framework is intended to make uncertainty visible, assigned, and monitorable; it does not make uncertainty disappear.

The current material was developed around Maritime Autonomous Surface Ships (MASS). The repository is arranged to support later work on deep-sea mining (DSM), pelagic ecology, and other ocean domains. Those future domains are not yet implemented: their current files are placeholders or planning material.

What OSB is not
Not a standard, IMO instrument, flag-State circular, classification-society rule, or approval.
Not legal advice, a certification basis, or a compliance guarantee.
Not a substitute for Administration approval, class survey, or another institution’s process.
Not independently reviewed or endorsed by an Administration, recognized organization, classification society, or standards body.
Not evidence that any vessel, system, or operation complies with an instrument.
Not a functioning software product. The specifications describe proposed system behavior; no operational OSB application or runtime is built in this repository.
Architecture
OSB groups four technical layers under a cross-cutting governance area. Each layer has a distinct purpose; the repository structure does not imply that every layer or domain is complete.

Area	Purpose	Current repository contents
Governance (Layer 0)	Frames OSB, records the domain inventory, and is intended to guide how domain packs are added.	Charter and domain registry scaffolds in 01-osb-governance/.
Layer 1 — Source and Friction Maps	Organizes domain-specific analysis of source material, uncertainty, and regulatory or scientific friction.	MASS Regulatory Bridge and change history are present. DSM has a placeholder only. Reference documents are catalogued separately in the grounding vault.
Layer 2 — Execution Pipeline	Specifies how claims could be produced, tested, monitored, and recorded.	ARCVB v0.1 draft; Oracle registry is a placeholder. This is not a deployed runtime.
Layer 3 — Consensus Protocol	Defines the shared claim-and-evidence framework, with domain-specific requirements separated into packs.	UCFS v0.3.1 core extraction, MASS material, the unchanged full source archive, and DSM/BIO placeholders.
Layer 4 — Adoption	Describes how the framework may be presented and discussed with institutions and counterparties.	IAAP v0.2.1 working draft; future counterparty-matrix extensions are a placeholder. No institutional engagement is documented here.
The intended relationship is:

Layer 4 — IAAP adoption layer
    ↓
Layer 3 — UCFS core + domain packs
    ↓
Layer 2 — ARCVB execution pipeline
    ↓
Layer 1 — domain-specific source and friction maps
The arrows show the conceptual stack, not implementation status or a dependency guarantee. For requirement-level dependencies, use the individual specifications.

Domain packs
UCFS is organized around a shared core and domain-specific material. The current state is:

Domain	Scope	Repository status
MASS-UCFS	Maritime Autonomous Surface Ships and related maritime obligations.	Core and extracted MASS material are present. The split preserves the original clause numbering and full source; references should be checked against the split record.
DSM-UCFS	Deep-sea mining, including proposed ISA-related and environmental topics.	Planned. Current domain files are placeholders; the build list is a provisional requirements brief, not verified evidence or a completed pack.
BIO-UCFS	Future sargassum and pelagic ecology work.	Placeholder only; no taxonomy or claims are defined.
Repository structure
OSB/
├── README.md
├── STRUCTURE.md
├── 00-grounding-vault/       Source copies, raw-note scaffolds, and source register
├── 01-osb-governance/        Charter and domain-registry scaffolds
├── build-notes/              Requirements for later development
├── demos/                    Illustrative demos grouped by domain
├── layer-1-source-friction-maps/
├── layer-2-execution-pipeline/
├── layer-3-consensus-protocol/
└── layer-4-adoption/
See STRUCTURE.md for the full folder-and-file inventory, placeholders, navigation links, and the UCFS split record. Update that file whenever files or folders are added, moved, renamed, or removed.

Grounding vault
The source register tracks the nine uploaded PDFs using local IDs GND-001 through GND-009. It records the uploaded filenames, identifying metadata, page counts, and SHA-256 checksums. The vault intake was not an independent authentication, current-status check, or full content review of those documents.

Key concepts in the specifications
These terms describe the proposed framework; their presence in documents does not mean software implementing them exists.

The [P] flag
[P] identifies a clause that relies on a source whose verification status has not been cleared under the UCFS process. A provisional clause cannot support a conformance claim until the source is verified or the approval authority accepts the provisional status through the specified route. See the UCFS core.

Non-waivable domains
Domain packs are intended to identify obligations that cannot be waived, compressed away, or bypassed within the framework. The MASS material carries NW-1 through NW-8. Proposed DSM non-waivables appear only in the build notes and have not been implemented or verified.

Bounded claims
A bounded claim records a controlled limitation where available evidence does not fully close an obligation. The specifications describe bounds, fallback behavior, monitoring, escalation, and re-open triggers as parts of that control. A bounded claim is not the same as an unresolved issue that has simply been ignored.

Runtime monitors and the ledger
ARCVB and UCFS describe runtime monitors that can detect declared threshold or claim changes and trigger escalation. They also describe an append-only, tamper-evident, investigator-usable ledger. These are specification concepts, not implemented capabilities in this repository; the specifications do not claim court admissibility.

Status and limitations
The specifications and analysis documents are drafts for technical review.
No document in this repository has been independently peer-reviewed or endorsed by an Administration, recognized organization, classification society, or standards body.
Some material was produced with an AI collaborator. This is development evidence, not independent corroboration.
No documented institutional engagement under the IAAP process is recorded in this repository. IAAP is proposed, not tested.
The MASS Regulatory Bridge identifies verification limits for its sources and analysis. Consult its verification section and the source register rather than treating its citations as independently checked.
The MASS rule-switching demo is illustrative and uses placeholder thresholds and simulated sensor noise. Its five scenarios pass on the fixed seeds, but one run in a 40-seed check missed the expected switch in scenario 2. It has not been validated against real traffic, measured sensor data, or Administration requirements; some behaviors described in the paper are not implemented in the demo.
The uploaded PDFs are retained as reference copies. Their presence in the vault does not establish authenticity, current legal status, or endorsement.
Navigation guide
If you are...	Start here
New to the repository	This README → STRUCTURE.md → OSB Ecosystem Charter
A regulator or Administration	MASS Regulatory Bridge → UCFS core and MASS pack
A classification society	UCFS core → IAAP
An autonomy developer or remote-operation provider	ARCVB → MASS Regulatory Bridge
A maritime lawyer or insurer	UCFS core → grounding-vault source register. The documents are not legal advice.
An ocean scientist	Grounding-vault source register → the relevant Layer 1 map. MASS is present; DSM is a placeholder.
A deep-sea mining stakeholder	DSM build notes and the DSM placeholders in Layer 1 and Layer 3. These are planning materials, not a completed DSM framework.
Conventions
MUST, MUST NOT, SHOULD, SHOULD NOT, MAY are used in the RFC 2119 sense where a specification says so.
[P] marks provisional source status as defined by UCFS.
Requirement IDs include ARCVB-<area>-<nn> for ARCVB and section identifiers for UCFS and IAAP.
The UCFS source/archive and split record preserve lineage. Do not silently replace or drop source material when revising a document.
A file marked [CONTENT] in STRUCTURE.md may still be a draft; the label means the file exists, not that it is approved or complete.
Document versions
Document	Version or date	Recorded status
UCFS	v0.3.1, 15 November 2026	Defect correction; no operative clause changed. The core/domain split is editorial.
ARCVB	v0.1, 14 November 2026	Initial implementation-architecture draft.
IAAP	v0.2.1, 14 November 2026	Defect correction and provisional-evidence update.
MASS Regulatory Bridge	13 November 2026; corrected 14 November	Working paper for technical review.
MASS rule-switching demo	15 November 2026	Illustrative simulation; see the limitations above and in the demo.
Use each document’s own status and revision history as authoritative for that document. The table is an orientation aid, not a substitute for those records.

Collaboration and engagement
OSB is intended as a working space for people dealing with intersections among ocean science, technology, regulation, industry, and policy. The repository does not establish a formal community or document that an institution has been engaged.

The working principles in the draft are:

Clear problem framing over slogans.
Evidence and constraints over positioning.
Practical interfaces that reduce unnecessary conflict.
Honest acknowledgment of trade-offs and uncertainty.
License and use
The repository license has not been declared. See the OSB Ecosystem Charter, which is currently a placeholder, for its planned non-normative role.

Do not present these drafts as an IMO instrument, flag-State circular, classification-society rule, legal advice, approval, certification basis, or evidence that a vessel or operation complies with any instrument.

Last updated: 16 November 2026
