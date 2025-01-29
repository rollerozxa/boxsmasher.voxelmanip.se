---
title: Debug features
---

The game contains some debug features that are useful for debugging, developing the game or for making levels for the game. Most code for the debug options are contained within the `dbg.lua` file, with some other debug functionality existing in other parts of the game where they are needed to be placed.

<!--more-->

## Enable debug features
If you are running the game from the source tree cloned with Git, debug features should be enabled by default.

Otherwise, you can create a file called `debug.txt` in the game's save directory (see [the LÖVE wiki](https://love2d.org/wiki/love.filesystem) where it is located) to enable debug features.

When debug features are active, there should be a red text that says "DEBUG" in the about screen accessible from the main menu.

![](/dev/debug.webp)

## Debug keybinds
Debug keybinds all use the F3 key as activator, with an arbitrary letter key to activate a specific debug option.

- `F3+C`: Display unscaled coordinates, scaled coordinates and the current coordinate in ozxa units, based on the current cursor position
- `F3+G`: Enable a debug grid sized in ozxa units
- `F3+F`: Show some debug info such as FPS and the current scaled resolution
- `F3+P`: Print positions of placed boxes
- `F3+I`: Pause physics iteration when in-game
- `F3+R`: Restart the current scene immediately
- `F3+T`: Automatically restart the current scene with 1 second intervals
