# Outer Rim 4K UI

A 2x interface mod for **The Outer Rim** (pre-CU Star Wars Galaxies emulator) so the UI is readable at 3840x2160.

It builds the 4K interface from your own Outer Rim install, so it always matches the client you're running. No Outer Rim game files are included in the installer.

## Downloads

| File | What it is |
| --- | --- |
| `OuterRim-4K-UI-Installer.zip` | Recommended. Builds the UI from your install. No Python needed, it carries its own. |

## Install

1. Close the game and the launcher.
2. Copy everything in the installer zip into your Outer Rim game folder (the one with `SwgClient_r.exe`).
3. Double-click one of:
   - `Install 4K UI.bat`
   - `Install 4K UI (with crafter layout).bat`
4. In `options.cfg`, set:
```
   screenWidth=3840
   screenHeight=2160
```
5. Start the game. After logging in, set the chat font size to 22.

## What it changes

- Every UI layout scaled 2x, with fonts remapped to sizes the client actually has
- Bigger inventory icon labels and stack counts
- Bigger login text
- Fixed overlap on the radial menu and the ship component flyout

**Crafter layout** (optional):
- Experimentation window shows all experiment lines without scrolling
- Assembly window fits up to ten ingredient slots and a larger resource stats panel
- Wider survey window so long resource names fit

If a crafting window opens at its old size, drag its corner once and the game remembers it.

## After an Outer Rim update

Run the same Install file again. It rebuilds from the updated game.

## Uninstall

Double-click `Remove 4K UI.bat`. It removes the 4K files and restores any loose UI files you had before. Nothing is ever deleted; replaced files are kept in `ui_scale_backup\previous`.

## Building from source

Requires Python 3.8+. From the game folder:

```
python tools\scale_ui.py                 build the 4K UI
python tools\scale_ui.py --crafting      also apply the crafter layout
python tools\scale_ui.py --pack          also write OuterRim-4K-UI.zip
python tools\scale_ui.py --revert        remove it
python tools\make_share_package.py       build OuterRim-4K-UI-Installer.zip
```

`scale_ui.py` reads the UI layouts from the archives listed in the client config (highest priority wins), scales pixel values 2x, and writes them as loose files in `ui\`, which the client loads in place of the archived copies. It only resizes and moves widgets, never renames them, so every element the client looks up still exists.

## Known limits

- The survey map's concentration numbers stay at their current size. The client has no larger bold font it can draw.
- Group frames follow the style set in the launcher at install time. Change it, then run Install again.
- I have only tested this with a brand new crafter. I will update it as I find and fix any other windwos/ui elements that need fixing. Feel free to message me with anything you find and I will address it.
## Disclaimer

Fan-made and not affiliated with The Outer Rim. Client-side UI only: no automation, no memory editing, no server interaction.
