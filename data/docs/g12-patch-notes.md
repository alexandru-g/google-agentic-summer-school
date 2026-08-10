# Silent Depths — Patch Notes

## v1.2.0 — 2026-01-15

This is the update we owed you.

- **Save system rewritten.** Save serialization is now atomic: a crash, alt-tab, or power loss during an autosave can no longer corrupt the file. Internal testing and beta-branch telemetry show zero corruptions across 40,000 save events.
- Added three manual save slots with automatic backup rotation; the last two autosaves are also kept as recoverable backups
- Corrupted saves from earlier versions: the launcher now attempts recovery from backup fragments — roughly 70% of affected files are restorable
- **Performance:** texture streaming pipeline rebuilt. VRAM usage reduced by ~30%; zone-transition hitching eliminated on 8 GB cards at Medium textures
- Minimum spec guidance updated to be honest about 8 GB vs 12 GB VRAM behavior

## v1.1.0 — 2025-09-03

- Autosave mitigation: saves now double-buffer to a temporary file before committing (reduces, but does not eliminate, corruption — full fix in development)
- Fixed the crash on Deck C of the Meridian tied to the ventilation cutscene
- Performance pass on the Brinefall approach; average fps up 12% on 8 GB cards
- Tidewalker chase: added a checkpoint before the flooded stairwell

## v1.0.4 — 2025-04-18

- Hotfix for the most common Deck C crash
- Fixed anglerkin audio positioning being mirrored on some 7.1 headsets
- Reduced flare drop variance in the early decks
