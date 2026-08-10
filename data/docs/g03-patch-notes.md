# Star Salvage Crew — Patch Notes

## v1.2 "Signal Lock" — 2026-01-09
- **Netcode overhaul:** movement and interaction are now server-authoritative, eliminating most desync and rubber-banding
- **Session reconnect:** if your connection drops, rejoin the same session within 10 minutes with inventory intact
- **Host migration:** if the host leaves or crashes, the session now transfers to another crew member instead of ending
- Fixed items appearing duplicated between clients and then vanishing on sale

## v1.1 — 2025-07-24
- New wreck: the Anemone, a flooded research vessel with security drones
- Friend Pass expanded from 2 to 3 free guest slots
- First round of desync mitigation: interpolation smoothing, cargo state reconciliation (further work ongoing)
- Voice chat vacuum muffling improvements

## v1.0.2 — 2025-03-18 (hotfix)
- Fixed a frequent disconnect when crossing airlock transitions with held cargo
- Patched a duplicate-salvage sale exploit
- Reduced connection timeouts during extraction sequences

## v1.0 — 2025-02-27
- Launch release: eight wrecks, four-player co-op, Friend Pass
