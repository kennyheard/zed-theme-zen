# Project Guidelines

## Project

A Zed editor theme. Single bundle at `themes/zen.json` containing Zen Dark and Zen Light. Published via `extension.toml` to the Zed marketplace at `zed-industries/extensions`.

## Palette

**Neutrals.** Tailwind-style scale from `#fafafa` (N50) to `#0a0a0a` (N950), plus `#ffffff` and `#000000`.

**Accent.** Teal. Primary is `#14b8a6` (T500). Functions and types use T400 (`#2dd4bf`) in dark mode and T600 (`#0d9488`) in light mode.

**State colours.** Tailwind 600 variants in light mode (red, green, blue, amber). Tailwind 400 variants in dark mode. Used for `error`, `success`, `info`, `warning` / `hint`, and version-control highlights.

**Symmetrical mapping.** Light and dark mirror across the scale: N50↔N950, N100↔N900, N200↔N800, N300↔N700, N400↔N600, N500 unchanged. Editor backgrounds at N50 / N950, panels at N100 / N900, frame at N200 / N800.

## Opacity Scale

- `1a` (10%) — player selections.
- `33` (20%) — UI state backgrounds, editor guides, scrollbar thumbs, word-level diff highlights.
- `66` (40%) — document highlights, created/deleted state backgrounds.
- `99` (60%) — reserved.
- `cc` (80%) — version-control indicators, search highlights, active line backgrounds.
- `ff` (100%) — solid colours, borders, syntax tokens, text.

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
