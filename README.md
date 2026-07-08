# myPitWall Agent — Releases

Compiled binaries for the myPitWall Agent (Windows installer), published automatically by CI from
the private `FOXSimRacing/myPitWall` repository on every version tag.

This repository contains no source code — only release artifacts (`.exe` + `manifest.json`) used
by the Agent's own auto-update mechanism.

## Latest Release

<!-- release-notes:start -->
## 0.13.1

### Patch Changes

- d9eba81: Fix a bug where a tray-icon initialization failure (e.g. the native tray binary failing to load the icon on some machines) crashed the whole agent and triggered an infinite restart loop, preventing the app from ever starting. Tray subsystem errors are now non-fatal.
<!-- release-notes:end -->
