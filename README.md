# myPitWall Agent — Releases

Compiled binaries for the myPitWall Agent (Windows installer), published automatically by CI from
the private `FOXSimRacing/myPitWall` repository on every version tag.

This repository contains no source code — only release artifacts (`.exe` + `manifest.json`) used
by the Agent's own auto-update mechanism.

## Latest Release

<!-- release-notes:start -->
## 0.14.6

### Patch Changes

- 86d4a90: fix(agent): actually fix the iracing-sdk-js Node ABI mismatch that v0.14.5 (4a54dc3) believed it had already resolved. That fix stripped `dependencies` from the staged app's package.json to stop electron-builder's own silent rebuild — which instead made its node-modules collector find nothing to collect and fall back to shipping the plain-Node-ABI addon straight from the monorepo's hoisted node_modules, the exact same crash from a different cause. Also fixes a second, previously undetected packaging bug (masked by the first crash happening earlier at startup): iracing-sdk-js's own `require('js-yaml')` failed once unpacked outside the asar, since js-yaml stayed packed inside it. Both the addon and js-yaml are now unpacked as siblings so the agent can actually reach a real iRacing session again. Verified end-to-end against a live session, not just a clean process start.
<!-- release-notes:end -->
