# Orbit Fall — Patch Notes

## v1.5.0 — 2026-02-10

Controller support is officially out of beta.

- Fixed gamepad detection failures on setups with multiple USB input devices; hot-plugging now works without restarting the game
- Added per-axis deadzone sliders and three response-curve presets (Linear, Classic, Feather)
- Input polling decoupled from vsync — measured input latency reduced by roughly 45 ms on 60 Hz displays
- Added an in-game input latency test in Options > Calibration
- New default framerate cap (240) to prevent frame-pacing judder on high-refresh monitors

## v1.4.2 (beta branch) — 2024-01-22

- Experimental gamepad support available via the `input-beta` opt-in branch
- Known issues: analog deadzone behaves inconsistently on some third-party pads; detection may fail after suspend/resume
- Fixed a physics edge case where wall-bounces at the apex of Gravity Well 7 lost momentum

## v1.2.1 — 2023-10-05

- Added two checkpoints to Gravity Well 7 following community feedback
- Magnetron Prime: reduced projectile density in phase two by 15%
- Added a "Steady Orbit" assist toggle (slows time by 10%, disables leaderboards)

## v1.0.3 — 2023-08-20

- Launch-week stability fixes
- Known issue: some players report gamepads not being detected at all. We are investigating; current workaround is keyboard input. We hear you — proper controller support is our top priority.
