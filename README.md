<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="/assets/icon-light.svg" />
    <source media="(prefers-color-scheme: light)" srcset="/assets/icon-dark.svg" />
    <img src="/assets/icon-dark.svg" alt="Zen icon" width="120" />
  </picture>
  <h1>Zen</h1>
  <p>A <a href="https://zed.dev">Zed</a> theme designed for clarity and focus.</p>
</div>

<br />

## Overview

Zen is made for engineers who value simplicity. Its muted palette and understated syntax create an environment that feels clear and unobtrusive.

- **Refined tones**: Neutral foundations with careful accents reduce visual strain.
- **Quiet syntax**: Structure is shown through gentle shifts in tone, without relying heavily on colour.
- **Minimal impression**: A restrained approach avoids noise and complexity.
- **Seamless modes**: Consistent contrast ensures smooth transitions between light and dark themes.
- **Complete coverage**: Every Zed feature is styled without gaps or omissions.

<br />

<figure>
  <img src="/assets/zen-light.png" alt="The Zen theme rendered in Zed's light mode" width="100%" />
  <p align="center"><sub><em>Zen Light.</em></sub></p>
</figure>

<br />

<figure>
  <img src="/assets/zen-dark.png" alt="The Zen theme rendered in Zed's dark mode" width="100%" />
  <p align="center"><sub><em>Zen Dark.</em></sub></p>
</figure>

<br />

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

<br />

## Editor Configuration (Optional)

The following configuration is one that I personally choose to complement Zen (as seen in the above previews):

```json
{
  "ui_font_family": "SF Pro Text",
  "ui_font_size": 14,
  "ui_font_weight": 400,
  "buffer_font_family": "Geist Mono",
  "buffer_font_size": 12,
  "buffer_font_weight": 400,
  "buffer_line_height": { "custom": 2.5 },
  "scroll_beyond_last_line": "off",
  "tabs": { "close_position": "left" },
  "project_panel": { "git_status": false },
}
```
