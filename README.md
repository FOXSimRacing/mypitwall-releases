# myPitWall Agent — Releases

Compiled binaries for the myPitWall Agent (Windows installer), published automatically by CI from
the private `FOXSimRacing/myPitWall` repository on every version tag.

This repository contains no source code — only release artifacts (`.exe` + `manifest.json`) used
by the Agent's own auto-update mechanism.

## Latest Release

<!-- release-notes:start -->
## 0.14.5

### Patch Changes

- 4a54dc3: fix(agent): prevent electron-builder from silently overwriting the rebuilt iracing-sdk-js with a version compiled for the wrong Node ABI. This resolves the issue where the agent could not connect to iRacing telemetry.
- 1beff30: fix: convert irsdk TypedArrays to JS Arrays for proper JSON serialization
- 3d69d29: fix(release): retry release with windows-2022 runner
<!-- release-notes:end -->
