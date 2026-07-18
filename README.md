# myPitWall Agent — Releases

Compiled binaries for the myPitWall Agent (Windows installer), published automatically by CI from
the private `FOXSimRacing/myPitWall` repository on every version tag.

This repository contains no source code — only release artifacts (`.exe` + `manifest.json`) used
by the Agent's own auto-update mechanism.

## Latest Release

<!-- release-notes:start -->
## 0.17.4

### Patch Changes

- d389abe: The lap times table's Piloto column header now reads "Equipe" in team/endurance sessions, and the column has a fixed 200px width with the full name available via a hover tooltip when truncated.
- d389abe: The lap times table now shows the team name instead of the current driver's name in team/endurance sessions, falling back to the driver name if no team name is set.
- d389abe: Cars on pit road or being towed now keep their class color on the track map (dimmed), instead of turning gray. Single-class sessions, where iRacing reports a white CarClassColor, now render that as yellow across the track map, lap times table, and relative table, instead of a near-invisible white.
- d389abe: The player's own marker on the track map is now slightly larger than the other cars', making it easier to spot at a glance.
- d389abe: Removed the sliding animation from car markers on the track map. Position updates now snap instantly instead of animating, which previously made a telemetry data jump (e.g. a stale lapDistPct while a car's data catches up after a tow or pit-road transition) look like the car was flying across the map.
<!-- release-notes:end -->
