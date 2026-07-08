# myPitWall Agent — Releases

Compiled binaries for the myPitWall Agent (Windows installer), published automatically by CI from
the private `FOXSimRacing/myPitWall` repository on every version tag.

This repository contains no source code — only release artifacts (`.exe` + `manifest.json`) used
by the Agent's own auto-update mechanism.

## Latest Release

<!-- release-notes:start -->
## 0.11.3

### Patch Changes

- bba881e: Add a `forceUpdateCheck` command, triggered automatically when the web app is opened with `?update=true` in the URL, so an update check can be forced from a link instead of waiting for the agent's periodic timer or the tray menu.
- 4ea71e9: Fix Lap Times table to match iRacing's own Standings box: row set is now the real driver roster (excluding spectators and the pace car) instead of the raw telemetry array, with a tie-break for equal/stale positions, the player's own row highlighted, and the Interval column showing iRacing's official gap field instead of an ad-hoc diff. Drivers who leave the session (disconnect, retire, etc.) now render with reduced opacity.
<!-- release-notes:end -->
