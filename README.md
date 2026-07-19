# myPitWall Agent — Releases

Compiled binaries for the myPitWall Agent (Windows installer), published automatically by CI from
the private `FOXSimRacing/myPitWall` repository on every version tag.

This repository contains no source code — only release artifacts (`.exe` + `manifest.json`) used
by the Agent's own auto-update mechanism.

## Latest Release

<!-- release-notes:start -->
## 0.17.7

### Patch Changes

- 11f0568: The agent can now set a native Discord reaction (🟢/🔴) on the tunnel-status message when a Discord bot token (`MYPITWALL_DISCORD_BOT_TOKEN`) is configured alongside the existing webhook — a plain webhook can't react to messages, only a real bot can. The redundant status-icon text line in the message itself was removed now that the reaction carries that signal. Opt-in: without a bot token, the agent just skips setting a reaction. Status-change reaction updates are now serialized (a race between two close-together status changes could otherwise leave more than one emoji on the message) and retry once/twice on a Discord rate-limit response instead of permanently dropping the update. The previous three-state status (🟢/🟡/🔴) is now binary (🟢/🔴) — an engineer only cares whether the driver is racing right now, so "app open, no session" now reads the same as "app closed": 🔴.
  - @mypitwall/shared@0.17.7
<!-- release-notes:end -->
