<div align="center">
  <img src="/assets/icon.svg" width="160" />
  <br />
  <h1>Zen</h1>
  <p>A <a href="https://zed.dev">Zed</a> theme inspired by the tranquil simplicity of Japanese zen gardens.</p>
</div>

## Features

Zen is crafted for developers who value simplicity and focus. It creates a clean workspace where visual noise fades away, allowing you to concentrate fully on your code.

- **Clean, spacious interface**: Thoughtful use of whitespace and gentle borders create breathing room around your work, reducing visual clutter and helping you maintain focus.
- **Restrained colour choices**: Built on a foundation of warm neutral tones with carefully placed teal accents that highlight important elements without overwhelming the overall aesthetic or breaking your concentration.
- **Quiet syntax highlighting**: Code elements use soft, muted tones that support readability while staying out of your way, allowing the structure and logic of your code to emerge naturally without unnecessary distractions.
- **Balanced light and dark modes**: Both themes share the same thoughtful contrast approach and include subtle interface details, ensuring a consistent experience whether you prefer light or dark environments.

## Previews

<div align="center">
  <img src="/assets/zen-light.png" alt="Zen Light" width="100%" />
  <p><em>Zen Light</em></p>
  <br />
  <img src="/assets/zen-dark.png" alt="Zen Dark" width="100%" />
  <p><em>Zen Dark</em></p>
</div>

## Installation

### Zed Extension (Recommended)

1. Open Zed.
2. Press `Cmd+Shift+P` (macOS) or `Ctrl+Shift+P` (Linux).
3. Type "Extensions" and select "zed: extensions".
4. Search for "Zen" and click "Install".
5. Select "Zen Dark" or "Zen Light" from the theme picker.

### Manual Installation

1. Download `zen.json` from the [latest release](https://github.com/kennyheard/zed-theme-zen/releases/latest).
2. Copy to your Zed themes directory:
   - **macOS**: `~/.config/zed/themes/`
   - **Linux**: `~/.config/zed/themes/`
3. Restart Zed and select the theme from the theme picker.

## Editor Configuration (Optional)

The following configuration is one that I personally choose to complement Zen's design philosophy:

```json
{
  "ui_font_family": "SF Pro",
  "ui_font_size": 14,
  "ui_font_weight": 400,
  "buffer_font_family": "Geist Mono",
  "buffer_font_size": 12,
  "buffer_font_weight": 400,
  "buffer_line_height": { "custom": 2.5 },
  "project_panel": { "git_status": false },
  "scroll_beyond_last_line": "off"
}
```

This configuration helps reduce visual noise to create an uncluttered, distraction-free experience.
