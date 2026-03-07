# Homebrew Tap

Custom Homebrew casks for the tap toolchain.

## Usage

### macOS (Homebrew)

```bash
# Add the tap (one-time setup)
brew tap hironow/tap

# Install tools
brew install --cask hironow/tap/phonewave
brew install --cask hironow/tap/sightjack
brew install --cask hironow/tap/amadeus
brew install --cask hironow/tap/paintress

# Update
brew update && brew upgrade --cask
```

### Any platform (Go)

```bash
go install github.com/hironow/phonewave@latest
go install github.com/hironow/sightjack@latest
go install github.com/hironow/amadeus@latest
go install github.com/hironow/paintress@latest
```

## Tools

| Tool | Description |
|------|-------------|
| [phonewave](https://github.com/hironow/phonewave) | D-Mail courier daemon |
| [sightjack](https://github.com/hironow/sightjack) | SIREN-inspired issue architecture tool for Linear |
| [amadeus](https://github.com/hironow/amadeus) | Divergence meter for your codebase |
| [paintress](https://github.com/hironow/paintress) | Claude Code expedition orchestrator |

## How it works

Casks in `Casks/` are automatically updated by [GoReleaser](https://goreleaser.com/)
when a new version is tagged in each tool's repository.

## License

Apache-2.0
