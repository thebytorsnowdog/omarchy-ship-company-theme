# Ship Company

A warm-kitchen Omarchy theme. Paper text on a dark wood background, gold on the window border, contribution green for success. Body text stays paper so the gold does not take over a coding session.

It comes from a few days in October 2026 when @thsottiaux bet he would ship something real every day for 28 days, and @poteto answered with comics: she is the Ship Company, he is the Reset Company. [The challenge](https://x.com/thsottiaux/status/2106845241357824205) and [the nothingburgers poster](https://x.com/poteto/status/2107566574735651107).

## Install

```sh
omarchy theme install https://github.com/thebytorsnowdog/omarchy-ship-company-theme.git
```

That clones it as `ship-company` and applies it. Switch back with whatever you were using before, for example:

```sh
omarchy theme set starship-ascendant
```

Cycle wallpapers with Super+Ctrl+Space, or `omarchy theme bg next`. Order is filename order: the shipping-event poster, the Ship Company / Reset Company poster, then the busywork comic, then the GPU-abacus scene.

## What is in here

`colors.toml` is the source of truth. Omarchy generates the terminal, neovim, vscode, and the rest from it when the theme is applied. This repo does not ship `hyprland.lua`, so gaps and corner radius stay at your defaults. The active border is gold falling into sweet-potato orange. `shell.bar.toml` only darkens the bar. Alerts on the bar stay a warm red, not gold.

Wallpaper art belongs to its creators and is not covered by the MIT licence on the config files. See CREDITS.md.
