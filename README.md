# hdrop

This script is meant to be started with keybindings and emulates the main feature of [tdrop](https://github.com/noctuid/tdrop) in [Hyprland](https://github.com/hyprwm/Hyprland), namely:

 - if the specified program is not running: launch it and bring it to the foreground.
 - if the specified program is already running on another workspace: bring it to the current workspace and focus it.
 - if the specified program is already on the current workspace: move it to workspace 'special:hdrop', thereby hiding it until called up again by hdrop.

Several instances of the same program can be run concurrently, if different class names are assigned to each instance. Presently there is support for the following flags:

 >`-a` ('foot' terminal emulator)
>
 >`--class` (all other programs)

 Example bindings in Hyprland config:

 >bind = $mainMod, b, exec, hdrop librewolf
>
 >bind = $mainMod, x, exec, hdrop kitty --class kitty_1
>
 >bind = $mainMod CTRL, x, exec, hdrop kitty --class kitty_2
 
# Installing

## Manual

Simple way: Download the script, make it executable and add it to your PATH.

Alternative: Clone the repo, cd to your desired tool, run `make` to build. To install, run
`make install`. You may need root privileges.

## hyprwm/contrib

`hdrop` is part of [hyprwm/contrib](https://github.com/hyprwm/contrib), which is a collection of useful scripts for `Hyprland`. There you can download a flake and add it to nix this way.
