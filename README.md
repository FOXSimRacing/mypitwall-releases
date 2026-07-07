# myPitWall Agent — Releases

Compiled binaries for the myPitWall Agent (Windows installer), published automatically by CI from
the private `FOXSimRacing/myPitWall` repository on every version tag.

This repository contains no source code — only release artifacts (`.exe` + `manifest.json`) used
by the Agent's own auto-update mechanism.

## Latest Release

<!-- release-notes:start -->
## 0.11.2

### Patch Changes

- 780f9c1: Stop the dashboard window from popping open automatically right after an auto-update — the app now stays minimized in the tray on that one relaunch, same as if the user had minimized it themselves.
  - @mypitwall/shared@0.11.2
- 36673d9: Replace the "connected" text indicator with a small dot that pulses mustard while the agent isn't connected to the sim and turns solid green once it is, and remove the redundant "Aguardando telemetria..." box — the dot now communicates connection status on both the driver and engineer dashboards.
  - @mypitwall/shared@0.11.2
<!-- release-notes:end -->
