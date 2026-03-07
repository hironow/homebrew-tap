# Homebrew Tap

Custom Homebrew formulae for the tap toolchain.

## Usage

```bash
# Add the tap (one-time setup)
brew tap hironow/tap

# Install tools
brew install hironow/tap/phonewave
brew install hironow/tap/sightjack
brew install hironow/tap/amadeus
brew install hironow/tap/paintress

# Update
brew update && brew upgrade
```

## Tools

| Tool | Description |
|------|-------------|
| [phonewave](https://github.com/hironow/phonewave) | D-Mail courier daemon |
| [sightjack](https://github.com/hironow/sightjack) | SIREN-inspired issue architecture tool for Linear |
| [amadeus](https://github.com/hironow/amadeus) | Divergence meter for your codebase |
| [paintress](https://github.com/hironow/paintress) | Claude Code expedition orchestrator |

## How it works

Formulae in `Formula/` are automatically updated by [GoReleaser](https://goreleaser.com/)
when a new version is tagged in each tool's repository.

## License

Apache-2.0
