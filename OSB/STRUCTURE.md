# OSB Folder and File Structure

This is the living table of contents for the OSB repository. Update it whenever files or folders are added, renamed, or moved.

## Status key

- **[NOW]** — exists in the repository.
- **[PLANNED]** — described or implied by the build notes, but not created yet.
- A planned entry is a place-holder in this map only; it does not mean that work has started.

## Current repository tree

```text
OSB/
├── README.md                                      [NOW] Short orientation
├── STRUCTURE.md                                   [NOW] This folder and file map
├── build-notes/
│   └── BUILDLIST NOTES 1.md                       [NOW] Future build requirements
├── demos/
│   └── MASS/
│       └── rule switching demo.html               [NOW] MASS rule-switching demo
├── layer-1-source-friction-maps/
│   └── MASS/
│       ├── Bridge_13Nov2026_change_log.md         [NOW] Changes for the 13 Nov paper
│       ├── MASS Regulatory Bridge 13Nov2026.md    [NOW] MASS source and friction map
│       └── versions/
│           └── MASS_REGULATORY_BRIDGE_v0_6.md     [NOW] Earlier standalone MASS draft
├── layer-2-execution-pipeline/
│   └── ARCVB v0.1.md                              [NOW] Execution pipeline specification
├── layer-3-consensus-protocol/
│   └── UCFS v0.3.1.md                             [NOW] Consensus protocol specification
└── layer-4-adoption/
    └── IAAP_v0_2_1.md                             [NOW] Institutional adoption protocol
```

## Planned expansion map

These are future slots, not existing files. Keep them marked **[PLANNED]** until they are actually created.

```text
OSB/
├── OSB_Mother_Node.md                             [PLANNED] OSB ecosystem and layer framing
├── layer-1-source-friction-maps/
│   └── DSM/
│       └── DSM Friction & Baseline Map.md         [PLANNED] DSM source and uncertainty map
├── layer-2-execution-pipeline/
│   └── ARCVB v0.1.md                              [NOW; future edits planned]
│       └── In-document additions:
│           ├── Oracle ingestion and provenance
│           ├── DSM environmental runtime monitors
│           └── DSM open items and lineage
├── layer-3-consensus-protocol/
│   └── UCFS v0.3.1.md                             [NOW; future edits planned]
│       └── In-document additions:
│           ├── DSM domain series and evidence tiers
│           ├── DSM non-waivable list and claim-model application
│           └── DSM open items, lineage, and revision record
└── layer-4-adoption/
    └── IAAP_v0_2_1.md                             [NOW; future edits planned]
        └── In-document additions:
            ├── ISA and mining-company engagement entries
            └── NOAA/data-authority distinction and DSM example
```

The planned additions above summarize the build list; they are not separate files unless a later design decision calls for that. The build list remains the source for scope and sequencing.

## How the documents connect

The layer numbering follows the build-list layout. The arrows below show its high-level path from adoption back to the source material:

```text
Layer 4 IAAP
    ↓
Layer 3 UCFS
    ↓
Layer 2 ARCVB
    ↓
Layer 1 source and friction maps (MASS now; DSM planned)
```

The documents also describe specific dependencies: ARCVB implements UCFS, IAAP refers to UCFS and ARCVB, and the Layer 1 maps provide source and friction context. Use the documents' own dependency statements when tracing a specific requirement; the folder numbers alone do not replace those references.

## File links

- [Build list](build-notes/BUILDLIST%20NOTES%201.md)
- [MASS Regulatory Bridge](layer-1-source-friction-maps/MASS/MASS%20Regulatory%20Bridge%2013Nov2026.md)
- [MASS change log](layer-1-source-friction-maps/MASS/Bridge_13Nov2026_change_log.md)
- [Earlier MASS v0.6 draft](layer-1-source-friction-maps/MASS/versions/MASS_REGULATORY_BRIDGE_v0_6.md)
- [MASS rule-switching demo](demos/MASS/rule%20switching%20demo.html)
- [ARCVB](layer-2-execution-pipeline/ARCVB%20v0.1.md)
- [UCFS](layer-3-consensus-protocol/UCFS%20v0.3.1.md)
- [IAAP](layer-4-adoption/IAAP_v0_2_1.md)
