# Audit

Checked `1d758fa58264b63c7c10e41f2f7dbb3f7f0f4072` on `main` on 29 October 2026. The tree is palette files, four wallpapers, and `preview.png`. History is two commits. No scripts, workflows, symlinks, or package files.

## Confirmed issues

None. No fix was opened.

## Checked and found fine

**Secrets.** The text files and both commits contain no keys, tokens, passwords, or private-key blocks. The JPEGs in `backgrounds/` have no EXIF, XMP, or comment segments. `preview.png` contains only `IHDR`, `IDAT`, and `IEND` chunks.

**Install contents.** Every tracked file is mode `100644`. Nothing is executable. There is no `.github` workflow and no symlink. A cloned Omarchy theme drops `*.lua`, terminal configs, `vscode.json`, and symlinks. This repository ships none of those.

**Colour files.** `colors.toml` uses six-digit hex values. `keyboard.rgb` is `edca2f`. Omarchy's keyboard scripts strip an optional leading `#` and then require six hex digits. `chromium.theme` is `237,202,47`, which is accent `#edca2f`, and the file ends with a newline. `shell.bar.toml` sets the same keys as the `[bar]` section of Omarchy `default/themed/shell.toml.tpl` on `master` at the time of this check, and changes the background to `#221b13`.

**Dependencies.** No lockfile, submodule, or package manifest.

**Assets.** `preview.png` is the theme-picker image. It is 1920 by 1080 and 1,526,963 bytes. A lossless re-save was 1,486,747 bytes, so the file was left as it is. Wallpaper sizes are `backgrounds/01-shipping-event.jpg` 417,477 bytes, `backgrounds/02-nothingburgers.jpg` 421,464 bytes, `backgrounds/03-bot-goes-down.jpg` 570,601 bytes, and `backgrounds/05-you-know-what-to-do.jpg` 412,226 bytes. All four are progressive JPEGs. Omarchy cycles `backgrounds/` in filename order. That order is `01`, `02`, `03`, then `05`, which matches the four wallpapers named in `README.md`.

## Looked at, not confirmed

These are not treated as defects. No pull request changes them.

**`icons.theme` names `Yaru-yellow-dark`.** Ubuntu Yaru has a directory by that name. The Omarchy manual lists `Yaru-yellow` and does not list `Yaru-yellow-dark`. First-party themes `everforest`, `ristretto`, `tokyo-night`, `catppuccin`, `rose-pine`, `nord`, `matte-black`, `vantablack`, and `gruvbox` use names with no accent `-dark` suffix. Omarchy copies this line into the GNOME `icon-theme` setting. If that name is not installed, the file manager does not get that icon set. This check did not list `/usr/share/icons` on an Omarchy machine.

**`btop.theme` has no `gradient_color_0` to `gradient_color_7`.** Those keys are in Omarchy `default/themed/btop.theme.tpl` on `master`. A shipped `btop.theme` stops generation of that file. btop was not run, so any effect on the graphs is unknown.

**`chromium.theme` uses the accent, not the background.** `chromium.theme.tpl` writes `background_rgb`. This file writes the gold accent. The value is valid. `README.md` does not say which colour the browser chrome should use.

**Wallpaper licence.** `LICENSE` and `CREDITS.md` already say the files in `backgrounds/` are not under the MIT licence. Deleting them would remove the wallpapers the theme ships.
