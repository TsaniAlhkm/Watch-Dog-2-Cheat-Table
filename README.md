# Watch Dogs 2 - Cheat Engine Table

A personal Cheat Engine table project for **Watch Dogs 2**.

This project was created as part of my reverse engineering learning journey. The main goal is to practice memory analysis, pointer tracing, Auto Assembler scripting, Lua scripting, coordinate manipulation, and runtime debugging in a local/offline environment.

## Features

This cheat table currently includes:

- Unlimited Health
- Unlimited Ammo
- Battery-related script
- Resources script
- Teleport to map marker
- Fly / vertical movement experiment
- Camera address experiment
- Speedhack / velocity experiment
- Additional experimental scripts

## Main Scripts

### Unlimited Health

Keeps the player health value stable during gameplay.

Learning focus:

- Pointer chain resolution
- Reading player health and max health
- Using Lua timers in Cheat Engine
- Writing float values safely
- Testing whether the health pointer remains stable after reloads

---

### Unlimited Ammo

Prevents ammo from decreasing when used.

Learning focus:

- Finding ammo write instructions
- Using Auto Assembler injection
- Understanding `dec` instructions
- Modifying resource consumption behavior
- Restoring original bytes when disabling the script

---

### Battery Script

A script related to battery or energy-like values.

Learning focus:

- Tracing float writes
- Identifying resource update functions
- Understanding `movss` instructions
- Testing value overwrite behavior

---

### Resources Script

An experimental script for resource-related values.

Learning focus:

- Analyzing resource subtraction logic
- Understanding conditional jumps
- Testing instruction flow changes
- Comparing original code behavior with patched behavior

---

### Teleport

A teleportation script that moves the player to the active map coordinate or marker.

Current concept:

- Enable the map coordinate script first
- Use the teleport script
- Press `F7` to teleport

Learning focus:

- Finding map marker coordinates
- Resolving player position pointer
- Reading X, Y, and Z coordinates
- Writing player position values
- Understanding coordinate structures

---

### Fly / Vertical Movement

An experimental movement script that changes the player's vertical position.

Learning focus:

- Reading and writing player position
- Using Lua timers for continuous movement
- Testing vertical coordinate changes
- Understanding movement stability and collision behavior

---

### Camera Address Experiment

A script for capturing camera-related values such as yaw/pitch address candidates.

Learning focus:

- Capturing effective addresses from assembly
- Saving camera-related addresses
- Reading float camera values
- Using camera direction for movement experiments

---

### Speedhack / Velocity Experiment

An experimental script for manipulating velocity-related values.

Learning focus:

- Resolving velocity pointer chains
- Reading velocity X/Y/Z
- Multiplying movement-related values
- Testing whether velocity manipulation is stable in gameplay

## Requirements

- Cheat Engine
- Watch Dogs 2
- Windows x64
- Basic understanding of Cheat Engine tables and script activation

## How to Use

1. Open Watch Dogs 2.
2. Open Cheat Engine.
3. Attach Cheat Engine to the game process.
4. Load the `.CT` file.
5. Enable the scripts you want to test.
6. For teleport, enable the coordinate/map script first, then use the teleport hotkey.

## Notes

Some scripts are experimental and may not work in every situation.

Possible causes:

- Different game version
- Different module address layout
- Pointer chain changed after restart
- Game loaded a different area
- Script activated before the required game object was loaded
- AOB signature no longer matches

If a script does not work, the first things to check are:

- Correct game process
- Correct module
- AOB scan result
- Pointer validity
- Whether the player is fully loaded in-game
- Whether the script needs another helper script enabled first

## Learning Goals

This project helped me practice:

- Cheat Engine memory scanning
- Pointer scan analysis
- Auto Assembler scripting
- Lua scripting in Cheat Engine
- AOB injection
- Register and offset analysis
- Float value manipulation
- Player coordinate manipulation
- Runtime debugging
- Safer script enable/disable structure

## Project Status

This is a learning project.

Some scripts are stable enough for testing, while others are still experimental and may need more debugging or cleanup.

## Disclaimer

This project is for educational reverse engineering and local memory analysis only.

The table and notes are intended for offline, single-player, and controlled testing environments. They should not be used for multiplayer cheating, online abuse, anti-cheat bypassing, piracy, account manipulation, or harming other players, developers, or services.

Reverse engineering should be practiced responsibly.
