# myPitWall Agent — Releases

Compiled binaries for the myPitWall Agent (Windows installer), published automatically by CI from
the private `FOXSimRacing/myPitWall` repository on every version tag.

This repository contains no source code — only release artifacts (`.exe` + `manifest.json`) used
by the Agent's own auto-update mechanism.

## Latest Release

<!-- release-notes:start -->
## 0.17.0

### Minor Changes

- 0cbc11f: Replace the live tow-time counter in the Standings table with a "T" badge that lights up once a car lands directly back in its pit stall after being towed (matching the detection approach used by irdashies), which is far less prone to false positives than timing `NotInWorld` directly (grid formation, practice/qualy resets, plain disconnects). The Standings "#" column (overall position) now only shows in multiclass races and has a leading zero like the class-position column; the Pit/Tow indicators are shortened to "P"/"T"; every dashboard panel now uses a `text-sm` base font size; and the Track Map now moves every car (including the player) along its own absolute track position instead of pinning the player at center, and hides a driver entirely once they've left the session.
- f92fcfa: Show live elapsed tow time ("TOW Xs") in the Standings table's last column when a driver is being towed back to the pits after a crash/off, instead of leaving that row blank for the whole tow. That column also got a fixed width so the text appearing/disappearing doesn't reflow the rest of the table.
- b610f9f: Track Map now marks every corner's position on the ring with its name as a tooltip, sourced from the lovely-track-data dataset (same source the open-source irdashies project uses, CC BY-NC-SA 4.0 — personal/non-commercial use only for now). The header now shows the track's real display name instead of iRacing's internal lowercase slug, and the session flag badges are centered in the header and no longer show non-race states (Servicible, StartHidden).

### Patch Changes

- 9617cd1: Replace the horizontal Track Map strip with a circular track map placed beside the Lap Times table. The dashboard page itself now scrolls vertically (with the header pinned to the top) instead of clipping every panel to fit one fixed viewport, and the panel layout has been reorganized around the new Track Map placement.
- 8e18af5: Move the Classificação drawer's toggle off the floating left-edge pull tab (reverted) back to a plain button, now overlaid top-right of the Mapa da Pista panel's own title row instead of the header.
- 6da153c: Turn the Lap Times ("Classificação") table into a full-height drawer toggled from a header button, closed by default, sliding in over everything else instead of taking up a permanent dashboard column. Track Map and Relativo now share that freed-up 3-column section, and the session flags banner moved to the always-visible header instead of overlaying the (now hidden-by-default) table.
- 6968a26: Move the Classificação drawer's toggle out of the header into a floating vertical pull-tab fixed to the left edge of the screen, vertically centered, always on top of the drawer/backdrop so it stays clickable in either state.
- 6d87255: Fix the Standings "Gap" column (renamed from "Intervalo"), which had regressed to a naive time diff that produced wrong values — including a false "-1 L" reading for a driver only a fraction of a second behind the leader, right when the leader crosses start/finish. Restored the lap-count-corrected gap formula and now derive "-N L" from that corrected gap instead of the raw lap-count difference. Also fixed the mock fixture's `CarIdxLap`, which had fallen out of sync with `CarIdxLapDistPct`'s own per-tick wraparound.
- 211e40b: Highlight the fastest lap of the race in purple in the Lap Times table's "Melhor volta" column. Track Map car markers now snap instantly instead of visibly sliding backward across the whole track on the tick a car wraps from ~100% back to ~0% at start/finish. The pedal/steering history chart's lines now transition smoothly between samples instead of snapping on every tick, matching the pedal bars and steering wheel.
- 5d5b74b: Move the circular Track Map to sit above the Radar de Proximidade panel (previously beside the Lap Times table), matching its box size and panel styling. Lap Times now takes the full width of its own column.
- 0a0ccf7: Fixed Track Map corner-name matching for multi-word track names (e.g. "Road Atlanta" could resolve to the wrong track), moved corner-name tooltips to an instant custom hover label instead of the browser's native delayed `title` tooltip, and fixed the header falling back correctly when the track's display name is blank.
- 366fed2: Track Map now fills the full width of its grid column and derives its height from that same width (no fixed pixel size or max-width cap), so it's always a perfect square that scales with the column instead of a fixed size that under- or over-fills it.
- 599d7d6: Give the Track Map its own top-level dashboard grid column (3 of 12), instead of nesting it inside Radar de Proximidade's column. The other three column groups are rebalanced from 4/4/4 to 3/3/3 to fit.
<!-- release-notes:end -->
