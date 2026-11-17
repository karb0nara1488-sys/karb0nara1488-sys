# DimensionBlocker

A lightweight Paper plugin for controlling access to the Nether and the End.

Created for use on a real SMP server.

## Features

- Enable or disable access to the Nether.
- Enable or disable access to the End.
- Prevents portal travel to a dimension while it is blocked.
- Saves both states in `plugins/DimensionBlocker/data.yml`.
- Announces dimension state changes to the server.

## Commands

| Command | Description |
|---|---|
| `/netherban` | Block access to the Nether |
| `/netherunban` | Allow access to the Nether |
| `/endban` | Block access to the End |
| `/endunban` | Allow access to the End |

## Permission

| Permission | Description | Default |
|---|---|---|
| `dimension.admin` | Use all DimensionBlocker commands | Operators |

## Installation

1. Download `DimensionBlocker.jar` from this repository.
2. Put the JAR into your server's `plugins` folder.
3. Restart the server.

The plugin creates its data file automatically.

## Compatibility

- Minecraft Java
- Paper API version: `1.21`

## Project notes

A small, practical server utility. It was used on an SMP server and kept intentionally simple.
