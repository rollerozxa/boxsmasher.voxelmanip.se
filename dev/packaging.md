---
title: Packaging
---

The `packaging/` folder in the source repository for the game contains various scripts for producing end-user consumable packages for the game.

<!--more-->

The resulting output of these scripts are then placed in a `packaging/bin/` folder excluded from source control.

## Universal LÖVE package

```bash
./make-game.sh
```

This script creates a universal LÖVE package (.love) of the game, which is a prerequisite for other scripts which packages the game for a particular platform.

## Windows

```bash
./make-win.sh
```

This script packages the game for Windows. It downloads the 64-bit LÖVE Windows runtime and fuses the game into the executable, editing it with `rcedit` and cleans up the folder for distribution.

## Linux

```bash
./make-linux.sh
```

This script packages the game for Linux. It downloads the 64-bit LÖVE Linux AppImage runtime, extracts it and modifies it to change metadata and bundle the game with it.

## Android
Packaging for Android is not stored in the main game repository as it builds a modified version of LÖVE from source. It can be found at [rollerozxa/boxsmasher-android](https://github.com/rollerozxa/boxsmasher-android).
