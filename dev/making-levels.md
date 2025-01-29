---
title: Making Levels
---

Currently there is no built-in level editor, making the process of creating levels a bit complicated as you will need to create and edit the level in a text editor. However there are some hidden debug features that make the process a bit smoother.

<!--more-->

## Level format
Currently levels are stored as Lua files in the `levels/` folder in the source tree.

For coordinates, point represent the topleft corner unless otherwise is stated.

- `author`: Author of the level
- `totalBalls`: Amount of balls provided to clear the level
- `throwBoundary`: Defines the boundary that the player can throw balls out of
	- `x`, `y`, `w`, `h`: Dimensions of the boundary
- `boxclusters`: List of box clusters.
	- Each element has the following values:
		- `x`, `y`: Coordinates of the topleftmost box
		- `w`, `h`: Dimensions of each box
		- `aX`, `aY`: Amount of boxes to place in each axis (Omitted values default to 1)
- `terrain`: List of rectangular static terrain pieces.
	- Each element has the following values:
		- `x`, `y`, `w`, `h`: Dimensions of the terrain
		- `colour`: Custom colour of terrain piece (optional)
		- `restitution`: Restitution/bounciness of the terrain piece (optional)
		- `friction`: Friction of the terrain piece (optional)

## Setting up the game for level editing
There are some hidden debug keybinds that are useful for level editing. To enable debug features in the game, see the [Debug](/dev/debug/) page.

- `F3+C`: Visualise coordinates. Prints the coordinate at the cursor in scaled coordinates, unscaled coordinates as well as in ozxa units.
- `F3+G`: Display a grid across the screen. Each cell is 1x1 ozxa units.
- `F3+I`: Pause physics simulation, so that physics-based elements stay in place until you have added support to them.

In addition to this there is also `F3+R` which restarts a level instantly. On each level restart, the game will reload the level from file, allowing you to hot-reload the current level you are editing without restarting the game. There is now also the `F3+T` keybind which will automatically restart a level in one second intervals. Make sure that your text editor does not have autosave enabled, as malformed Lua code in a level file will crash the game.

## ozxa units
You're likely going to see existing levels measuring things in multiples of 40. This has been coined the ozxa unit, named after the game's author, and is useful for layouting and designing levels according to a grid.

One ozxa unit is 40 unscaled pixels, and the internal resolution of 1280x720 fits 32x18 ozxa units. This is what the debug grid uses, and the coordinate visualiser will tell you what the currently highlighted cell is in ozxa units.
