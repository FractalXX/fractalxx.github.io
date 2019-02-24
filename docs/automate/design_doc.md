# Automate

[TOC]

## Mantra
Automate is a tech-oriented top down sandbox game, where the player's objective is to build an industry which does not need human interference.

## Design pillars
The following phrases describe the game experience:
- Planning: plan ahead to build an efficient industry
- Technology: use high-tech machines and solutions to automate production
- Satisfaction: the player should feel the progress when looking at their industry
- No luck: random number generator usage should be minimized (but not erased)

## Summary
The game is a top down sandbox and building game, centered around technology and science. There are no characters in the game, just the player: one who can use their surroundings to build an industry, which does its job on its own.

## Mechanics
The player starts with a simple building which allows for basic storage and crafting. The objective is to expand: at first, the player has to gather resources manually to get started, then start to automate resource production to build advanced things.

### Start
When the game starts, a finite world is randomly generated loaded with resources and everything the player needs to start off. The world consists of blocks.

### Controls
After the world loads, the player can use its mouse to navigate around the map. The entire map is revealed instantly (no fog of war). The player has an inventory and a hot bar.

List of controls (default):
- Left mouse button: select a block, open the block's UI (if it has one)
- Left mouse button double click: pick a block (if it can be picked)
- Right mouse button: place selected block from hotbar
- F1: open inventory
- Mouse wheel: zoom
- Q and E: rotate camera
- R and F: tilt camera

Some blocks might have extra controls specific to their UI, those are not listed here.

### Types of blocks
Blocks can be any of the following types:
- Basic: solid, has no extra functionality, can be used for decoration
- Special: same as Basic, but has extra functionality (machines, pipes, etc.)
- Multiblock:
 - made up from multiple blocks but represented as one
 - may or may not have extra functionality
- Liquid:
 - no extra functionality
 - can flow
 - can be filled with solid blocks

#### Special blocks
This group primarily consists of machines. Machines are single, special blocks which perform a task on a variety of inputs and produces an output. An input and an output can be an item, multiple items, liquids, or energy.

Another special group of blocks is pipes. Pipes can transfer items, liquids, or gases. They attach to any input or output on machines and can be configured to either pull or push.

Wires are used to transfer electric energy which powers machines. They attach to any side of a machine and they can either pull or push energy. Pull or push is decided automatically, depending on the machine.

#### Multiblocks
These are made up from multiple blocks but represented as one. They could also be considered as single blocks which are *n x n* blocks in size.
Regarding behaviour, they can be picked and placed as a single block.

### Multiplayer
The game can be played in coop multiplayer either through a dedicated server or hosting directly in the client.

## Interface
While ingame, the player uses its mouse to navigate around the map and manage blocks.

[TODO: UI Wireframe]

## Development plan

### Target platform
The game is compatible with the 3 major desktop operating systems:
- Windows
- Linux
- MacOS

Support for mobile devices is also a plan for the future:
- Android
- iOS

### Used technologies
The game is written entirely in C# on top of the Monogame framework. Monogame allows for building games for any of the major desktop operating systems, with minimal effort needed for porting.

For the game server, the .NET Socket library is used, which is compatible with Mono as well, meaning the server can be ran on Windows, Linux, and MacOS, too.

