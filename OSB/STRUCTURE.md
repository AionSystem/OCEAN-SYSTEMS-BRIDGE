# OSB Folder and File Structure

Living table of contents for the OSB workspace. Update this file whenever folders or files are added, renamed, or moved.

## Status key

- **[CONTENT]** — existing project material.
- **[EXTRACTED]** — moved verbatim from the full UCFS source into a modular file.
- **[SOURCE ARCHIVE]** — unchanged source retained for comparison.
- **[PLACEHOLDER]** — scaffold only; not source material and not a completed specification.

## Adopted tree

```text
OSB/
├── README.md                                             [CONTENT] Short orientation
├── STRUCTURE.md                                          [CONTENT] This map
│
├── 00-grounding-vault/
│   ├── raw-notes/
│   │   └── 2025-06_DSM_Seminar_Notes.md                  [PLACEHOLDER] Source notes not present yet
│   ├── external-standards/
│   │   └── PLACEHOLDER_ISA_NOAA_IEC.md                   [PLACEHOLDER] Import actual source text later
│   └── case-law/
│       └── PLACEHOLDER_EVER_SMART_PENN.md                [PLACEHOLDER] Import actual case-law text later
│
├── 01-osb-governance/
│   ├── OSB_Ecosystem_Charter.md                          [PLACEHOLDER] Non-normative OSB framing
│   └── Domain_Registry.md                                [PLACEHOLDER] Starter domain index
│
├── build-notes/
│   └── BUILDLIST_NOTES_1.md                              [CONTENT] Future build requirements
│
├── demos/
│   └── MASS/
│       └── rule_switching_demo.html                      [CONTENT] MASS rule-switching demo
│
├── layer-1-source-friction-maps/
│   ├── MASS/
│   │   ├── MASS_Regulatory_Bridge_13Nov2026.md           [CONTENT] MASS source/friction map
│   │   ├── Bridge_13Nov2026_change_log.md                [CONTENT] Change history for the paper
│   │   └── versions/
│   │       └── MASS_REGULATORY_BRIDGE_v0_6.md            [CONTENT] Earlier standalone draft
│   └── DSM/
│       └── DSM_Friction_Map_v0.1.md                      [PLACEHOLDER] No DSM claims drafted here
│
├── layer-2-execution-pipeline/
│   ├── ARCVB_Core_v0.1.md                                [CONTENT] Existing ARCVB document, renamed only
│   └── oracles/
│       └── Oracle_Registry.md                            [PLACEHOLDER] No Oracle registry defined yet
│
├── layer-3-consensus-protocol/
│   ├── UCFS_Core_v0.3.1.md                               [EXTRACTED] Shared/core text with routing notes
│   ├── source/
│   │   └── UCFS_v0.3.1_Full_Source.md                    [SOURCE ARCHIVE] Unchanged full UCFS source
│   └── domain-packs/
│       ├── MASS-UCFS/
│       │   └── MASS_Domains_and_NWs.md                   [EXTRACTED] MASS domains, NWs, and related clauses
│       ├── DSM-UCFS/
│       │   └── DSM_Domains_and_NWs.md                    [PLACEHOLDER] DSM pack not built yet
│       └── BIO-UCFS/
│           └── BIO_Domains_Placeholder.md                [PLACEHOLDER] Future ecology domain
│
└── layer-4-adoption/
    ├── IAAP_Core_v0.2.1.md                               [CONTENT] Existing IAAP document, renamed only
    └── counterparties/
        └── IAAP_Matrix_Extensions.md                     [PLACEHOLDER] Future matrix additions
```

## Navigation links

### Grounding and governance

- [DSM seminar notes placeholder](00-grounding-vault/raw-notes/2025-06_DSM_Seminar_Notes.md)
- [External standards placeholder](00-grounding-vault/external-standards/PLACEHOLDER_ISA_NOAA_IEC.md)
- [Case-law placeholder](00-grounding-vault/case-law/PLACEHOLDER_EVER_SMART_PENN.md)
- [OSB ecosystem charter placeholder](01-osb-governance/OSB_Ecosystem_Charter.md)
- [Domain registry](01-osb-governance/Domain_Registry.md)
- [Build list](build-notes/BUILDLIST_NOTES_1.md)

### Layer documents

- [MASS source map](layer-1-source-friction-maps/MASS/MASS_Regulatory_Bridge_13Nov2026.md)
- [MASS change log](layer-1-source-friction-maps/MASS/Bridge_13Nov2026_change_log.md)
- [Earlier MASS v0.6 draft](layer-1-source-friction-maps/MASS/versions/MASS_REGULATORY_BRIDGE_v0_6.md)
- [DSM friction-map placeholder](layer-1-source-friction-maps/DSM/DSM_Friction_Map_v0.1.md)
- [ARCVB core document](layer-2-execution-pipeline/ARCVB_Core_v0.1.md)
- [Oracle registry placeholder](layer-2-execution-pipeline/oracles/Oracle_Registry.md)
- [UCFS core](layer-3-consensus-protocol/UCFS_Core_v0.3.1.md)
- [Full UCFS v0.3.1 source archive](layer-3-consensus-protocol/source/UCFS_v0.3.1_Full_Source.md)
- [MASS-UCFS domain pack](layer-3-consensus-protocol/domain-packs/MASS-UCFS/MASS_Domains_and_NWs.md)
- [DSM-UCFS placeholder](layer-3-consensus-protocol/domain-packs/DSM-UCFS/DSM_Domains_and_NWs.md)
- [BIO-UCFS placeholder](layer-3-consensus-protocol/domain-packs/BIO-UCFS/BIO_Domains_Placeholder.md)
- [IAAP core document](layer-4-adoption/IAAP_Core_v0.2.1.md)
- [IAAP matrix-extension placeholder](layer-4-adoption/counterparties/IAAP_Matrix_Extensions.md)
- [MASS rule-switching demo](demos/MASS/rule_switching_demo.html)

## UCFS split record

The original `UCFS v0.3.1` file is preserved unchanged at `layer-3-consensus-protocol/source/UCFS_v0.3.1_Full_Source.md`. The new core and MASS pack are an editorial extraction, not a new substantive revision or an independent review. Moved clauses retain their original section numbers.

| Original UCFS material | New location |
|---|---|
| §5.4.1 non-waivable list | MASS pack §5.4.1 |
| §§6.3–6.4 MASS domains and sub-items | MASS pack §§6.3–6.4 |
| §8.5.5 MASS minimum-tier table and §8.5.7 tier restriction | MASS pack §§8.5.5 and 8.5.7 |
| §§10–23 domain-specific clauses | MASS pack §§10–23 |
| Annexes A–F, H, and P | Same annexes in the MASS pack |

The shared gate and non-waivable mechanisms remain in the core. Historical annexes retained in the core may refer to the source numbering; use the split record and archived source to trace those references.

## How the layers connect

```text
Layer 4 — IAAP adoption layer
    ↓
Layer 3 — UCFS core + domain packs
    ↓
Layer 2 — ARCVB execution pipeline
    ↓
Layer 1 — domain-specific source and friction maps
```

The layer numbers show the repository organization. For requirement-level dependencies, use the references in the individual specifications.
