# Chess Royale 100 — Patch Notes

## v2.5 — 2026-04-22

- Added the Replay Tribunal: flagged games are anonymized and reviewed by high-rank community panels; verdicts feed the ban system
- Matchmaking Rating v3: placement matches now seed by measured move accuracy instead of win count — new players should no longer meet thousand-win veterans in their first sessions
- Bot backfill now clearly labels bot opponents in the post-game summary
- Fortress engine-detection model retrained; detection latency down from days to hours

## v2.3 — 2025-05-14

- Matchmaking rework: rank bands tightened, smurf-detection heuristics added
- Bot backfill reduced by 60% below rank 5; queue times may increase slightly at off-peak hours
- Fixed a bug where the same three bot profiles appeared repeatedly in consecutive lobbies
- Cosmetic crown-shard drop rate doubled

## v2.0 "Fortress" — 2024-08-19

Our largest integrity update ever.

- Introduced Fortress: server-side move analysis that flags statistically inhuman play across a match, not single moves
- First ban wave completed: 14,182 accounts removed
- Report flow shortened to two clicks; reporters now receive outcome notifications
- Known limitation: detection favors precision over speed; sophisticated cheaters may take multiple games to flag. Ongoing work.

## v1.4 — 2023-12-06

- Bot backfill tuning: bots now blunder at human-plausible rates (we are aware this sentence is funny)
- Queue time improvements at low ranks
- Fixed final-circle draw conditions when both kings fall into the void simultaneously
