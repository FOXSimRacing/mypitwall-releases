# myPitWall Agent — Releases

Compiled binaries for the myPitWall Agent (Windows installer), published automatically by CI from
the private `FOXSimRacing/myPitWall` repository on every version tag.

This repository contains no source code — only release artifacts (`.exe` + `manifest.json`) used
by the Agent's own auto-update mechanism.

## Latest Release

<!-- release-notes:start -->
## 0.14.7

### Patch Changes

- 10d0199: fix(agent): fix auto-update always failing to download since the electron-builder migration. electron-builder's default nsis artifactName includes a space ("myPitWall Setup X.Y.Z.exe"); it writes a separate GitHub-safe (hyphenated) filename into latest.yml assuming it will be the one publishing, but release-agent.yml instead uploads the raw file manually via `gh release create`, which sanitizes the space into a dot instead — leaving three different filenames in play (space, hyphen, dot) and electron-updater downloading a 404. artifactName is now pinned to an already-safe, no-spaces pattern so the built file, the latest.yml entry, and the uploaded GitHub asset all agree.
<!-- release-notes:end -->
