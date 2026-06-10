# Handover

**Last updated:** 2026-06-10 (JST)
**Updated by:** claude (AI draft from git history — review before trusting)

## Current State

The tap distributes four cask-installable tools: amadeus, paintress,
phonewave, sightjack (`Casks/*.rb`), plus `tap_migrations.json` mapping the
old formula names. The entire git history consists of automated
"Brew cask update for <tool> version vX.Y.Z" commits pushed by GoReleaser
from the tool repositories. Last commit: `8873839` "Brew cask update for
paintress version v0.0.12" on 2026-04-04. `Formula/` is empty. CI is a
single `audit.yaml` workflow plus dependabot config under `.github/`.

## In Progress

不明 (git 履歴からは判別できず) — all commits are automated cask bumps; no
manual work appears to be in flight.

## Next Actions

1. requester による docs/intent.md ドラフトのレビューと確定

## Known Risks / Blockers

- Casks are overwritten by GoReleaser on each upstream release — manual cask edits will not survive; change the GoReleaser config in the tool repos instead

## Context the Next Actor Needs

- This repo is almost entirely machine-managed; human changes normally touch only README, `.github/`, or `tap_migrations.json`
- The four distributed tools live in their own repos: hironow/phonewave, hironow/sightjack, hironow/amadeus, hironow/paintress
- Users can also install via `go install github.com/hironow/<tool>@latest` (README)

## Relevant Files and Commands

- `Casks/{amadeus,paintress,phonewave,sightjack}.rb` — GoReleaser-managed cask definitions
- `tap_migrations.json` — formula-to-cask migration mapping
- `.github/workflows/audit.yaml` — CI audit workflow
- `brew tap hironow/tap && brew install --cask hironow/tap/<tool>` — user-facing install path
