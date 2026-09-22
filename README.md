<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="/assets/icon-light.svg" />
    <source media="(prefers-color-scheme: light)" srcset="/assets/icon-dark.svg" />
    <img src="/assets/icon-dark.svg" alt="Zen icon" width="100" />
  </picture>
  <h1>Zen</h1>
  <p>A <a href="https://zed.dev">Zed</a> theme designed for clarity and focus.</p>
  <p>
    <a href="https://github.com/kennyheard/zed-theme-zen/releases/latest"><img src="https://img.shields.io/github/v/release/kennyheard/zed-theme-zen?style=flat-square&labelColor=1a1a1a&color=666666" alt="Latest release" /></a>
    <a href="./LICENSE"><img src="https://img.shields.io/github/license/kennyheard/zed-theme-zen?style=flat-square&labelColor=1a1a1a&color=666666" alt="License: MIT" /></a>
  </p>
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
  <picture>
    <img src="/assets/zen-light.png" alt="The Zen theme rendered in Zed's light mode" />
  </picture>
  <p align="center"><sub><em>Zen Light.</em></sub></p>
</figure>

<br />

<figure>
  <picture>
    <img src="/assets/zen-dark.png" alt="The Zen theme rendered in Zed's dark mode" />
  </picture>
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

### Automatic Switching

To have Zed switch between them with your system appearance, set both in your settings.

```json
{
  "theme": {
    "mode": "system",
    "light": "Zen Light",
    "dark": "Zen Dark"
  }
}
```

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
  "project_panel": { "git_status": false }
}
```

<br />

## License

MIT © Kenny Heard. See [LICENSE](./LICENSE).

<br />

## Acknowledgements

Zen's greys, teal accent, and state colours are taken from the [Tailwind CSS](https://tailwindcss.com) colour palette, distributed under the [MIT License](https://github.com/tailwindlabs/tailwindcss/blob/main/LICENSE). Its coverage and key order follow the One theme that ships with [Zed](https://github.com/zed-industries/zed). The Zen icon is by [Adrien Coquet](https://thenounproject.com/browse/icons/term/zen) via Noun Project, used under [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/).
