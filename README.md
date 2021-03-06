# Dante's build of dwm BASED on Luke Smith's Build

## Dante's notes:

- This is a fork of [Luke Smith's dwm build] (https://github.com/lukesmithxyz/dwm)
- **This build removes the title bar at the top that displays information on the focused window**
- Pretty much the only changes are some custom keybinds for launching applications
e.g discord and exiting dwm is `win-shift-e`
- Check `config.h` for keybinds and settings etc.

## Custom patch applied:

- [No title](https://dwm.suckless.org/patches/notitle/) - This patch hide window title on top bar.

## FAQ

> What are the bindings?

The source code is the documentation! Check out [config.h](config.h).

Okay, okay, actually I keep a readme in `larbs.mom` for my whole system, including the binds here.
Press `super+F1` to view it in dwm (zathura is required for that binding).
I haven't kept `man dwm`/`dwm.1` updated though. PRs welcome on that, lol.

## Patches and features

- Clickable statusbar with my build of [dwmblocks](https://github.com/lukesmithxyz/dwmblocks).
- Reads xresources colors/variables (i.e. works with `pywal`, etc.).
- scratchpad: Accessible with mod+shift+enter.
- **Note: These Layouts are disabled in this current build**
 			
	*- New layouts: bstack, fibonacci, deck, centered master and more. All bound to keys `super+(shift+)t/y/u/i`.*
- True fullscreen (`super+f`) and prevents focus shifting.
- Windows can be made sticky (`super+s`).
- stacker: Move windows up the stack manually (`super-K/J`).
- shiftview: Cycle through tags (`super+n/p`).
- vanitygaps: Gaps allowed across all layouts.
- swallow patch: if a program run from a terminal would make it inoperable, it temporarily takes its place to save space.

## Installation for newbs

```
git clone https://github.com/dantefernando/dwmNoTitle
cd dwmNoTitle
sudo make install
```

## Please install `libxft-bgra`!

This build of dwm does not block color emoji in the status/info bar, so you must install [libxft-bgra](https://aur.archlinux.org/packages/libxft-bgra/) from the AUR, which fixes a libxft color emoji rendering problem, otherwise dwm will crash upon trying to render one. Hopefully this fix will be in all libxft soon enough.
