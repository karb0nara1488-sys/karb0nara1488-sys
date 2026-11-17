# RelicDungeons

A configurable dungeon system for Minecraft Java servers running Paper.

RelicDungeons creates separate dungeon instances from reusable room templates. Players can explore generated layouts, play solo or in parties, fight bosses, collect loot and use relics with passive and active abilities.

**Current version:** `0.1.0-SNAPSHOT`  
**Minecraft:** Java 1.21  
**Platform:** Paper

## Features

- Procedurally generated dungeon layouts built from room templates.
- Separate dungeon instances with a configurable world pool.
- Solo runs and party runs, with configurable party size.
- Room types: start, normal, special and final.
- Configurable dungeon difficulty, room count, time limits and unlock requirements.
- Boss encounters with health phases, abilities, minions and configurable rewards.
- Loot chests placed throughout dungeons and completion rewards.
- Relics with passive effects and right-click active abilities.
- Player, party and dungeon progress statistics.
- English and Russian message files.
- Configuration validation with a report of detected problems.

## Current content

The included configuration currently contains one dungeon: **Sunken Catacombs**, with the **Storm Core** boss encounter.

At this stage, there is one configured dungeon type and one configured boss. The system is designed to be expanded: server owners can add their own dungeon and boss definitions in the configuration files, and create additional room templates in-game.

## Adding your own dungeons and bosses

Dungeon definitions are stored in `dungeons.yml`. Boss definitions are stored in `bosses.yml`.

You can add entries with your own IDs and settings, then connect a dungeon to a boss using the `boss` field. Dungeon layouts are assembled from room templates.

Room templates can be created in-game using the template editor commands. The editor supports selecting a region, defining door connections, saving templates with a room type and optional tags, listing templates and validating them.

Useful template commands:

- `/rd template wand`
- `/rd template save <id> <start|normal|special|final> [weight] [tag1,tag2]`
- `/rd template list`
- `/rd template validate <id>`

For the full command list, use `/rd help`.

## Main commands

- `/rd help` - show command help.
- `/rd dungeon list` - list configured dungeons.
- `/rd dungeon info <id>` - show dungeon information.
- `/rd dungeon start <id> [seed]` - start a dungeon.
- `/rd party <create|invite|accept|decline|leave|kick|leader|disband|info>` - manage a party.
- `/rd menu` - open the plugin menu.
- `/rd relic list` - list configured relics.
- `/rd loot list` - list loot tables.
- `/rd stats` - view player statistics.
- `/rd reload` - reload supported configuration values.

Administrative commands require `relicdungeons.admin`. Players need `relicdungeons.play` to use dungeon gameplay commands.

## Configuration files

The plugin generates its configuration files in `plugins/RelicDungeons/`:

- `config.yml` - general settings, worlds, instances, parties and generator options.
- `dungeons.yml` - dungeon definitions and generation settings.
- `bosses.yml` - boss entities, phases, abilities and rewards.
- `loot.yml` - loot tables and chest settings.
- `relics.yml` - relic items, passive effects and active abilities.
- `messages.yml` and `messages_ru.yml` - messages and translations.
- `templates/` - saved room template data.

Configuration is validated on startup. Some settings can be reloaded, while settings that affect worlds or stored item data require a server restart.

## Installation

1. Download `RelicDungeons.jar` from this repository.
2. Place it in the server's `plugins` folder.
3. Start or restart the server.
4. Configure the generated files in `plugins/RelicDungeons/`.
5. Create or configure room templates before starting a dungeon.

## Project status

RelicDungeons is under active development and will receive further updates. The current build is an early snapshot, so features, configuration options and documentation may change between versions.

## Permissions

- `relicdungeons.play` - allows players to enter dungeons and use player commands. Default: everyone.
- `relicdungeons.admin` - full administrative access, including the room template editor. Default: operators.

## Notes

- Built for Paper API 1.21.
- Folia is not supported by this build.
- Dungeon worlds are temporary and are cleaned up according to the plugin's world settings.
