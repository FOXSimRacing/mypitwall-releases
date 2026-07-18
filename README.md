# myPitWall Agent — Releases

Compiled binaries for the myPitWall Agent (Windows installer), published automatically by CI from
the private `FOXSimRacing/myPitWall` repository on every version tag.

This repository contains no source code — only release artifacts (`.exe` + `manifest.json`) used
by the Agent's own auto-update mechanism.

## Latest Release

<!-- release-notes:start -->
## 0.17.5

### Patch Changes

- 7a7cc94: The Discord tunnel-ready notification is now sent as soon as the tunnel comes up (instead of waiting for an active session) and shows a status icon before the link — 🟢 online with an active session, 🟡 online with no session loaded yet, 🔴 offline or link unreachable. The message is edited in place as the status changes instead of only being sent once, and it's now kept (edited to 🔴) rather than deleted when the tunnel goes down or the agent shuts down — it's only replaced once a new tunnel link is actually generated.
  - @mypitwall/shared@0.17.5
<!-- release-notes:end -->
