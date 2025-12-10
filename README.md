# viewing-macos-screenshots

A Claude Code plugin that lets Claude view and analyze your macOS screenshots.

## Installation

### Personal Usage

To install this plugin for your personal use in Claude Code:

1. Add the marketplace:

```
/plugin marketplace add chadpod/viewing-macos-screenshots-claude-code-plugin
```

2. Install the plugin:

```
/plugin install viewing-macos-screenshots@viewing-macos-screenshots-claude-code-plugin
```

### Team Usage

To make this plugin available for your team, add to your project's `.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "viewing-macos-screenshots-claude-code-plugin": {
      "source": {
        "source": "github",
        "repo": "chadpod/viewing-macos-screenshots-claude-code-plugin"
      }
    }
  },
  "enabledPlugins": {
    "viewing-macos-screenshots-claude-code-plugin:viewing-macos-screenshots": true
  }
}
```

## Usage

Once installed, just ask Claude to look at your screenshots:

- "Look at my screenshot"
- "What's in my latest screenshot?"
- "Examine my last 3 screenshots"
- "I just took a screenshot, can you help me with it?"

Claude will automatically find and read your most recent screenshot(s) from wherever macOS saves them (Desktop by default).

## How It Works

The skill:
1. Checks your macOS screenshot save location (`defaults read com.apple.screencapture location`)
2. Finds the most recent `Screenshot*.png` or `Screen Shot*.png` files
3. Reads the image(s) so Claude can see and analyze them

## License

MIT License - see [LICENSE](LICENSE) for details.

## Author

Chad Podoski ([@chadpod](https://github.com/chadpod))
