# myPitWall Agent — Releases

Compiled binaries for the myPitWall Agent (Windows installer), published automatically by CI from
the private `FOXSimRacing/myPitWall` repository on every version tag.

This repository contains no source code — only release artifacts (`.exe` + `manifest.json`) used
by the Agent's own auto-update mechanism.

## Latest Release

<!-- release-notes:start -->
## 0.14.0

### Minor Changes

- d401b6a: Add a horizontal track map to the engineer dashboard: the whole lap is compressed onto a single bar with the player fixed at the center, other cars shown as class-colored dots (labeled with their class position) at their physical track position, and pit-road cars rendered dimmed/gray.

### Patch Changes

- b9c3230: Fix a bug where a Cloudflare tunnel startup failure always surfaced a generic 30-second timeout message blaming a missing `cloudflared` dependency, even when the real cause was something else (e.g. Cloudflare rate-limiting new Quick Tunnel requests). The tunnel error shown in the engineer dashboard now reflects the actual cause, including a specific message for Cloudflare rate limiting.
<!-- release-notes:end -->
