<div align="center">
  <img src="/assets/icon.svg" width="180" />
  <br />
  <h1>Zen</h1>
  <p>A <a href="https://zed.dev">Zed</a> theme inspired by the clarity and calm of Japanese zen gardens.</p>
</div>

## Features

Zen is made for engineers who value simplicity and focus. Its muted palette and understated syntax create an environment that feels clear and unobtrusive.

- **Refined tones**: Neutral foundations with careful accents reduce visual strain.
- **Quiet syntax**: Structure is shown through gentle shifts in tone, without relying heavily on colour.
- **Minimal impression**: A restrained approach avoids noise and complexity.
- **Tuned contrast**: Consistency across light and dark modes creates a seamless experience.

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

The following configuration is one that I personally choose to complement Zen (as seen in the above previews):

```json
{
  "ui_font_size": 14,
  "ui_font_weight": 400,
  "ui_font_family": "SF Pro",
  "buffer_font_size": 12,
  "buffer_font_weight": 400,
  "buffer_font_family": "Geist Mono",
  "buffer_line_height": { "custom": 2.5 },
  "title_bar": { "show_branch_icon": true },
  "tabs": { "close_position": "left" },
  "project_panel": { "git_status": false },
  "scroll_beyond_last_line": "off",
}
```
