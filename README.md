# myPitWall Agent — Releases

Compiled binaries for the myPitWall Agent (Windows installer), published automatically by CI from
the private `FOXSimRacing/myPitWall` repository on every version tag.

This repository contains no source code — only release artifacts (`.exe` + `manifest.json`) used
by the Agent's own auto-update mechanism.

## Latest Release

<!-- release-notes:start -->
## 0.11.4

### Patch Changes

- 6b0e319: Correct comments/docs about tire pressure/temperature/wear telemetry being live vs. snapshot-only, based on a real live session capture (334-field raw dump + continuous monitoring across a full lap). No behavior change: the field-mapping fallback chain was already correct, only the explanation of why was wrong (attributed to anti-cheat instead of iRacing simply not exposing a live hot-pressure channel at all, and temp/wear turning out to be snapshot-only too, not live as initially misjudged from a single sample).
  - @mypitwall/shared@0.11.4
- eefa4bd: Fix Lap Times table showing each driver's own best lap time as the "Intervalo" instead of a real gap (CarIdxF2Time can report either depending on session context — now derived from CarIdxEstTime relative to the leader instead). Fix Relative table's Gap sign being inverted compared to iRacing's own Relative overlay (ahead of the player is now positive, behind is negative).
- 1b41284: Fix Relative table ordering and Gap value using CarIdxLap as a cross-driver reference — correct only in race sessions (a shared/synchronized race distance), but meaningless in practice/qualify (a personal, per-driver counter). Ordering and Gap now always use physical track proximity (CarIdxLapDistPct/CarIdxEstTime with start/finish-line wraparound), in every session type.
  - @mypitwall/shared@0.11.4
<!-- release-notes:end -->
