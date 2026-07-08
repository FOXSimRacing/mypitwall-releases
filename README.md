# myPitWall Agent — Releases

Compiled binaries for the myPitWall Agent (Windows installer), published automatically by CI from
the private `FOXSimRacing/myPitWall` repository on every version tag.

This repository contains no source code — only release artifacts (`.exe` + `manifest.json`) used
by the Agent's own auto-update mechanism.

## Latest Release

<!-- release-notes:start -->
## 0.13.0

### Minor Changes

- c77dc0f: Add multiclass color-coding to Tabela de Classificação and Tabela Relativa: a class-colored position badge showing rank within category (not overall), a new "#" overall-position column, a "-N L" lapped indicator matching iRacing's own Standings box, and a live PIT timer tracked agent-side so it survives a browser refresh. Also fixes CarClassColor/SessionLaps/SessionTime being misparsed as strings on a real session.

### Patch Changes

- 9268038: Make dashboard panel titles semibold for better visual hierarchy.
<!-- release-notes:end -->
