
# AzerothCore Module Ghost Speed

- Latest build status with azerothcore:

[![Build Status](
https://github.com/sogladev/mod-ghost-speed/actions/workflows/core-build.yml/badge.svg?branch=master&event=push)](https://github.com/sogladev/mod-ghost-speed)

This is a module for [AzerothCore](http://www.azerothcore.org) that changes the speed while dead

- Modifies Ghost speed to use custom values


## How to install
https://www.azerothcore.org/wiki/installing-a-module

1. Requires source recompilation
2. Modify config
  found in `/etc/modules`, copy `.conf.dist` to `.conf` and edit
3. Apply database changes
  this should be done automaticly `data/sql/db-world/base/ghost_speed.sql`

## How to remove

1. Undo database changes: `optional/undo_ghost_speed.sql`

2. Remove `mod-ghost-speed` folder

## Resources
ghost speed is set by aura 8326

Night Elves are applied `ID - 20584 Ghost` with Blizzard Default speed of 75 (+50% increase)

Highest speed value is applied

example of usage in the core
- https://github.com/azerothcore/azerothcore-wotlk/blob/a196f7f28aa263dc7f9c532e15839f3b409fb68f/src/server/game/Handlers/CharacterHandler.cpp#L957

modifying the bp set by this aura with an AuraScript sets a custom speed

Spellwork 8326

![8326 spell info](8326_ghost.png)

## How to create your own module

1. Use the script `create_module.sh` located in [`modules/`](https://github.com/azerothcore/azerothcore-wotlk/tree/master/modules) to start quickly with all the files you need and your git repo configured correctly (heavily recommended).
1. You can then use these scripts to start your project: https://github.com/azerothcore/azerothcore-boilerplates
1. Do not hesitate to compare with some of our newer/bigger/famous modules.
1. Edit the `README.md` and other files (`include.sh` etc...) to fit your module. Note: the README is automatically created from `README_example.md` when you use the script `create_module.sh`.
1. Publish your module to our [catalogue](https://github.com/azerothcore/modules-catalogue).

