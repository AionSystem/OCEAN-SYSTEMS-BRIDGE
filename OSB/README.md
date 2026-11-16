# OSB Repository Map

OSB is the parent folder for the system documents. The four layer folders follow the architecture described in `build-notes/BUILDLIST NOTES 1.md`.

For the complete folder-and-file tree, including planned future slots, see [`STRUCTURE.md`](STRUCTURE.md).

## Layers

1. **Source and friction maps** — `layer-1-source-friction-maps/`
   - `MASS/` contains the MASS Regulatory Bridge paper and its change log.
   - `MASS/versions/` keeps the earlier standalone v0.6 draft separate.
   - A DSM friction map is planned in the build notes; it has not been created.
2. **Execution pipeline** — `layer-2-execution-pipeline/` contains ARCVB.
3. **Consensus protocol** — `layer-3-consensus-protocol/` contains UCFS.
4. **Adoption layer** — `layer-4-adoption/` contains IAAP.

## Supporting material

- `build-notes/` contains the build list for future work. Its requirements have not been implemented as part of this organization pass.
- `demos/MASS/` contains the rule-switching HTML demo associated with the MASS material.

Only file locations and repository navigation were changed; document contents were preserved.
