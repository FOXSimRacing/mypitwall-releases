# myPitWall Agent — Releases

Compiled binaries for the myPitWall Agent (Windows installer), published automatically by CI from
the private `FOXSimRacing/myPitWall` repository on every version tag.

This repository contains no source code — only release artifacts (`.exe` + `manifest.json`) used
by the Agent's own auto-update mechanism.

## Latest Release

<!-- release-notes:start -->
## 0.17.1

### Patch Changes

- 54e07d5: Fixed the Cloudflare Quick Tunnel silently going dead after staying up for a while (process crash or the tunnel just stopping routing traffic) with no automatic recovery. The agent now watches the tunnel's own process for an unexpected exit and periodically pings its public URL end-to-end; either signal triggers regenerating a fresh tunnel, re-notifying Discord with the new link, and reflecting a non-blocking "reconnecting" state on the dashboard instead of the old link staying stuck as "ready" forever.
<!-- release-notes:end -->
