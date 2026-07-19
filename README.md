# myPitWall Agent — Releases

Compiled binaries for the myPitWall Agent (Windows installer), published automatically by CI from
the private `FOXSimRacing/myPitWall` repository on every version tag.

This repository contains no source code — only release artifacts (`.exe` + `manifest.json`) used
by the Agent's own auto-update mechanism.

## Latest Release

<!-- release-notes:start -->
## 0.17.6

### Patch Changes

- f1cd024: The Discord tunnel webhook message now keeps naming the driver in its 🟡/🔴 states instead of falling back to a generic "myPitWall" subject — the last resolved driver name is persisted across agent restarts and reused whenever no session is currently loaded.
- 26b806f: The status icon (🟢/🟡/🔴) in the Discord tunnel webhook message now shows on its own line below the link, instead of before it.
- 0d1df76: Fixed the Pit Strategy panel showing the same estimated pit-lane time loss for all three fuel styles (Lift & Coast, Média Atual, Full Push) regardless of how much fuel each one adds. The time loss is now computed per style, matching the fuel amount actually shown for that style.
<!-- release-notes:end -->
