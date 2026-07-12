# myPitWall Agent — Releases

Compiled binaries for the myPitWall Agent (Windows installer), published automatically by CI from
the private `FOXSimRacing/myPitWall` repository on every version tag.

This repository contains no source code — only release artifacts (`.exe` + `manifest.json`) used
by the Agent's own auto-update mechanism.

## Latest Release

<!-- release-notes:start -->
## 0.15.0

### Minor Changes

- 3fbbdb2: Add driver ratings (SR, iRating), SOF, Split info, and historical pit time estimates to dashboards.
- 85266b0: Implementação do motor de Estratégia de Box (Pit Strategy Engine)
  - Rastreamento dinâmico de tempo de Pit (Drive-through)
  - Estratégias automáticas (Undercut, Defesa, Overcut)
  - Redesign do PitWindowPanel na Web.

### Patch Changes

- 4d30a61: feat(agent): replace the default Electron File/Edit/View/Window/Help menu with just File > Sair and Help > Sobre o myPitWall, removing devtools/zoom/window-management items that don't apply to this single-window dashboard app.
- e2fc331: fix(agent): stop a driver's Última volta/Melhor volta time from blanking out in the standings table the moment they enter the pits, by caching each car's last known valid lap time agent-side (fixes #155).
- 9ebb118: fix(web): pit command panel no longer freezes every field out of syncing with the driver's Black Box (PitSvFlags/PitSvFuel) just because the engineer is editing one unrelated field. Also makes mock/dev mode (`yarn dev:mock`) actually simulate PitSvFlags/PitSvFuel from a sent pit command, so this can be verified without a live iRacing session.
- c9b33c1: fix(agent,web): clear the live PIT-road timer once the local driver exits the car (unless it's a team/endurance event where a driver swap is expected) or an opponent disconnects, instead of letting it keep counting indefinitely (fixes #153). Also reformats the PIT time display: raw seconds under 1 minute (unchanged), `m:ss` from 1 to 59 minutes, `h:mm` from 60 minutes on — applied to both the live standings column and the historical average pit-lane stat.
- 86ce9ea: fix(web): hide the Melhor volta/Intervalo columns in the standings table during Practice/Qualify sessions, where gap-to-leader and session-best-of-all concepts don't apply since every driver is running independent laps.
- d69a15b: Ajustes e refinamentos no PitWindowPanel e IncidentPanel, incluindo correções no cálculo de combustível e sincronização com o estilo de pilotagem.
<!-- release-notes:end -->
