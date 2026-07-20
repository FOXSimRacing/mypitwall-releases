# myPitWall Agent — Releases

Compiled binaries for the myPitWall Agent (Windows installer), published automatically by CI from
the private `FOXSimRacing/myPitWall` repository on every version tag.

This repository contains no source code — only release artifacts (`.exe` + `manifest.json`) used
by the Agent's own auto-update mechanism.

## Latest Release

<!-- release-notes:start -->
## 0.17.10

### Patch Changes

- 9cd1abc: The Discord tunnel-status message is now edited in place with the new link when a fresh tunnel comes up (e.g. after a reconnect), instead of deleting the old message and posting a new one — the channel keeps a single persistent message per driver/agent. Falls back to posting a new message only if there wasn't one yet, or the previous one is gone (e.g. manually deleted in Discord).
- 0adacb0: The classification table drawer ("Tabela de Classificação") now sizes itself to its content width instead of being capped at a fixed 576px that was already narrower than the table's own columns, with a viewport-relative cap (95vw) and horizontal scroll as a fallback on narrow windows. Also added a manual `workflow_dispatch` trigger to the release-agent CI workflow so an already-published version's installer can be rebuilt/republished on demand (e.g. after adding a repo secret that didn't exist at the time of the original release) without a version bump.
<!-- release-notes:end -->
