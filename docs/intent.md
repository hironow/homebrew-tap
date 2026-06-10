# Intent

**Last updated:** 2026-06-10
**Requester:** hironow
**Status:** DRAFT — AI が README / git 履歴から起草。requester 未確認
**Work unit:** homebrew-tap — Homebrew tap distributing casks for the tap toolchain

## Goal

Distribute the tap toolchain binaries (phonewave, sightjack, amadeus,
paintress) to macOS users via `brew tap hironow/tap`, with casks in `Casks/`
updated automatically by GoReleaser whenever a new version is tagged in each
tool's repository.

## Success Criteria

- `brew install --cask hironow/tap/<tool>` works for the four tools listed in README (phonewave, sightjack, amadeus, paintress)
- Casks stay in sync with upstream releases — git history shows GoReleaser-driven cask bumps per tagged version (latest: v0.0.12 across all four tools)
- The `audit.yaml` GitHub Actions workflow passes
- Beyond these: 未定義 — Open Questions 参照

## Scope

### In scope

- Cask definitions in `Casks/` for the four tools, `tap_migrations.json`, and the audit workflow

### Out of scope (Non-goals)

- Building or releasing the tools themselves — each tool's own repository tags releases and GoReleaser pushes cask updates here
- `Formula/` is currently empty — only casks are distributed (未確認: whether formulas are planned)

## Constraints

- Cask updates are automated by GoReleaser from the tool repositories; manual edits may be overwritten on the next release
- Apache-2.0 license (per README)

## Open Questions

- [ ] requester による本ドラフトのレビュー
- [ ] Is the empty `Formula/` directory intentional (casks-only tap), or are formulas planned?
- [ ] No release activity since 2026-04-04 (v0.0.12) — is the tap current with the latest tool releases?
- [ ] Exact scope/intent of `tap_migrations.json` entries — drafted from file contents only
