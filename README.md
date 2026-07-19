# myPitWall Agent — Releases

Compiled binaries for the myPitWall Agent (Windows installer), published automatically by CI from
the private `FOXSimRacing/myPitWall` repository on every version tag.

This repository contains no source code — only release artifacts (`.exe` + `manifest.json`) used
by the Agent's own auto-update mechanism.

## Latest Release

<!-- release-notes:start -->
## 0.17.8

### Patch Changes

- 90b1387: The Discord tunnel-status webhook message no longer spells out "está correndo agora!" / "está offline." in its text — that's already conveyed by the 🟢/🔴 reaction. Instead it now reports the agent's version (e.g. "está utilizando a v1.2.3"), useful for spotting a driver running a stale build. The link line is unchanged.
  - @mypitwall/shared@0.17.8
<!-- release-notes:end -->
