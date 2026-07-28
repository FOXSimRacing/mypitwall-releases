# myPitWall Agent — Releases

Compiled binaries for the myPitWall Agent (Windows installer), published automatically by CI from
the private `FOXSimRacing/myPitWall` repository on every version tag.

This repository contains no source code — only release artifacts (`.exe` + `manifest.json`) used
by the Agent's own auto-update mechanism.

## Latest Release

<!-- release-notes:start -->
## 0.19.0

### Minor Changes

- 6996130: The classification table ("Tabela de Classificação") now has feature parity with the user's standalone standings overlay: Gap/Interval are computed relative to each car's own class instead of the overall leader, plus new Volta, sector-time (S1..Sn), and Flags (off-track/black/dq/repair/DNS/OFFLINE) columns, a class-record purple flash on Melhor volta and sector cells, class filter pills, sticky header/left columns, zebra striping, a row-slide animation on position changes, and smoothed Gap/Interval counting between telemetry ticks. Pit stop duration now shows the lap it was entered on (`L<lap> <time>`) instead of a bare `P <time>`.
<!-- release-notes:end -->
