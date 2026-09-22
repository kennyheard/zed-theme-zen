# Project Guidelines

## Project

A Zed editor theme. Single bundle at `themes/zen.json` containing Zen Dark and Zen Light. Published via `extension.toml` to the Zed marketplace at `zed-industries/extensions`.

## Palette

**Neutrals.** Zinc scale from `#fafafa` (Z50) to `#09090b` (Z950), plus `#ffffff` and `#000000`.

**Accent.** Teal. Primary is `#14b8a6` (T500). Functions and types use T400 (`#2dd4bf`) in dark mode and T600 (`#0d9488`) in light mode.

**State colours.** 600 variants in light mode (red, green, blue, amber). 400 variants in dark mode. Used for `error`, `success`, `info`, `warning` / `hint`, and version-control highlights.

**Symmetrical mapping.** Light and dark mirror across the scale: Z50↔Z950, Z100↔Z900, Z200↔Z800, Z300↔Z700, Z400↔Z600, Z500 unchanged. Editor, active tab, and toolbar backgrounds at Z50 / Z950, panels at Z100 / Z900, frame at Z200 / Z800.

## Opacity Scale

- `1a` (10%) — player selections, ghost element hover/selected, resting scrollbar thumb.
- `33` (20%) — status backgrounds, editor guides, active search match, document read highlights, word-level diff highlights.
- `66` (40%) — element hover/active/selected, scrollbar thumb border, document write highlights, created/deleted state backgrounds.
- `99` (60%) — scrollbar track, scrollbar thumb hover/active.
- `cc` (80%) — borders, version-control added/deleted indicators, search highlights, active line backgrounds, drop targets.
- `ff` (100%) — solid colours, focus borders, syntax tokens, text. Keep syntax and text solid; opacity on text renders unpredictably.

## Key Ordering

Top-level style block follows the upstream Rust struct order from `crates/settings_content/src/theme.rs::ThemeColorsContent` — match a recent default theme when adding a key. Status colour tail (`conflict` through `warning`) and the syntax block are both alphabetical.

## Schema Updates

Only adopt keys that at least one official default theme (One, Ayu, Gruvbox) actually sets. Most schema fields are deliberately left to Zed's fallbacks. The One theme is the reference for Zen's coverage.

## Releases

1. Bump `extension.toml` version.
2. Commit `Bumped extension version to vx.x.x` and push.
3. Tag and push: `git tag vx.x.x && git push origin vx.x.x`.
4. `gh release create vx.x.x --title "vx.x.x" --notes "..."`.

Release notes cover theme changes only. Plain bullets. No `## Added / Changed / Fixed` headings. No "Full Changelog" link. If no theme files changed in the range, the body reads `No theme changes. Packaging and documentation refinements only.`

## Marketplace Submission

PR to `zed-industries/extensions` from `kennyheard/extensions`.

1. Sync the fork by cloning via SSH, fetching upstream, hard-resetting to `upstream/main`, force-pushing. (`gh repo sync` fails on a missing `workflow` scope.)
2. Bump the `[zen]` block's `version` in `extensions.toml`.
3. Update the submodule pointer: `git update-index --cacheinfo 160000,<tag-sha>,extensions/zen`.
4. Commit `Update Zen theme extension` and push.
5. `gh pr create --repo zed-industries/extensions --base main --head kennyheard:main --title "Update Zen to vx.x.x" --body "Request to update the theme extension, Zen."`
