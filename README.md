# fldocs

**fldocs** is a CLI tool that lets you search and read Flutter and Jetpack Compose documentation offline — no browser needed. It downloads the full docs to your machine and gives you instant local search from the terminal.

## Key Features

- Search Flutter and Jetpack Compose docs instantly from your terminal
- Read full documentation pages without opening a browser
- Works completely offline after the initial sync
- Filter results by source — Flutter or Compose only
- Integrates with Claude Code and other AI assistants as an MCP server
- Single binary — no runtime dependencies required

## Requirements

- macOS, Linux, or Windows

## Installation

### Homebrew
```bash
brew install AndroidPoet/tap/fldocs
```

### Download binary
Download the latest release from [GitHub Releases](https://github.com/AndroidPoet/fldocs/releases).

## Usage

**Search both**
```bash
fldocs search "animation"
fldocs search "lazy column"
fldocs search "state management"
```

**Search by source**
```bash
fldocs search "navigation" --source flutter
fldocs search "modifier" --source compose
```

**Read a page**
```bash
fldocs get ui/widgets/basics
fldocs get compose/layouts/basics
```

**Browse all pages**
```bash
fldocs ls
fldocs ls --source compose
```

**Stats**
```bash
fldocs stats
```

## Claude Code Integration

Add to your Claude Code MCP settings:

```json
{
  "mcpServers": {
    "fldocs": {
      "command": "/usr/local/bin/fldocs",
      "args": ["mcp"]
    }
  }
}
```

Claude can now search and read Flutter and Compose docs directly inside your conversations.
