# 3d-save-schema

The engine-independent envelope of a game save, as JSON Schema 2020-12 (`save.schema.json`).

An envelope holds `schemaVersion`, `gameId`, `slotId`, `savedAt`, `payloadVersion` and a game-owned `payload`. The schema never describes the payload, so any runtime can read the envelope, but only the game knows what is inside.

`examples/` has a valid save. The Unity adapter is [`3d-unity-save`](../3d-unity-save).

### Status

v1 draft: one envelope, one example.

### Roadmap

- Invalid fixtures and a validation script.
- Optional integrity fields (checksum) if cloud sync needs them.
