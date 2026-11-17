# MaceLimiter

A small gameplay-balancing plugin that limits the server to one player-crafted mace.

Created for use on a real SMP server.

## Features

- Allows only the first successful mace craft by a non-operator.
- Prevents shift-click crafting of the mace.
- Stores the crafted state in `plugins/MaceLimiter/data.yml`, so it persists after restarts.
- Restricts common ways of moving or disposing of the mace, including dropping it, inventory transfers, bundles, item frames, death drops and auction-house selling through `/ah sell`.
- Operators are exempt from the restrictions.

## Commands

This plugin does not register any commands.

## Configuration and data

The plugin creates `data.yml` automatically and stores the `mace_crafted` state. There is no user-editable configuration file.

## Installation

1. Download `MaceLimiter.jar` from this repository.
2. Put the JAR into your server's `plugins` folder.
3. Restart the server.

## Compatibility

- Minecraft Java
- Paper API version: `1.21`

## Project notes

A lightweight SMP utility focused on keeping the mace rare and preventing it from circulating freely between players.
