# Rank Plugin for Metamod with MySQL Integration

This project is not yet ready to be tested on a real server, it is still in development.
There's not a lot of work left before releasing a BETA :)

## Overview
**Developed in partnership with [VeryGames](https://www.verygames.net).**

This is a rank plugin designed to work with Metamod, incorporating a MySQL database for data storage. The plugin provides a point system that tracks player performance in a Counter-Strike 2. It includes various features to manage and update player ranks based on their in-game actions.

***Thank to CS2Fixe project (Poggy & Xen) for providing a solid code base.***

# Want to contribute ?
- If you want to contribute, you can check the todo list and make a pull request once you have made a feature.

- If a feature is not on the todo list, you can create an issue to discuss and check if we implement your idea :)

- If you don't have the required skills in C++, you can just test the plugin and create issues if needed :)

# TODO List

#### Security
- [X]  For hibernation to false
- [X]  Unload plugin if there is no mysql connection

#### Configuration
- [x]  Mysql
- [x]  Core
- [x]  Phrases
- [x]  Points

#### Core
- [x]  Rank stats
- [x]  Sessions stats
- [x]  Translation system
- [x]  Colors
- [x]  Cross server ranking
- [ ]  Deathmatch FFA support
- [ ]  Documentation

#### Commands
- [x]  Antiflood system
- [x]  !rankh
- [x]  !rankannouce
- [x]  !rank
- [x]  !stats
- [x]  !top
- [x]  !restrank
- [x]  !topsession
- [x]  !ranksession
- [x]  !statsession

#### Event triggers
- [x]  Player death by weapon
  - [x]  Attacker
  - [x]  Victim
  - [X]  Assist
- [x]  Player death by headshot
  - [x]  Attacker
  - [x]  Victim
  - [X]  Assist
- [x]  Player death by knife
  - [x]  Attacker
  - [x]  Victim
  - [X]  Assist
- [x]  Bomb planted
  - [x]  Team
  - [x]  Planter
- [x]  Bomb Exploded
  - [x]  Team
  - [X]  Planter
  -  Need to fix the phrases that are not sent
- [x]  Bomb Defused
  - [x]  Team
  - [x]  Defuser

#### Stats triggers
- [x]  Register last connection
- [ ]  Stats per weapons
- [x]  Headshot
- [x]  Knife
- [x]  Kill T
- [x]  Kill CT
- [x]  Death T
- [x]  Death CT
- [x]  Death Suicide
- [x]  Bomb planted
- [x]  Bomb exploded
- [x]  Bomb defused
- [x]  Teamkill T
- [x]  Teamkill CT

#### Web page
- [x]  Theme
- [x]  Lazy load images
- [ ]  Global rank system
  - [x]  Table with rank
  - [ ]  Player searching
  - [x]  Pagination
- [ ]  Stats page per user (After the end of statistics)

#### Discord Bot
- [x]  Translation
- [x]  Command `/rank`
- [x]  Command `/top`
- [x]  Command `/ranklink`

## Require
- CS2 Serveur (Linux or Window)
- Remove server hibernation `sv_hibernate_when_empty 0`
- mysql_mm plugins by Poggu : https://github.com/Poggicek/mysql_mm

## Features
Provide rank and stats system.

A web interface is available https://github.com/Salvatore-Als/cs2-rank/tree/main/external/web

A discord bot is available https://github.com/Salvatore-Als/cs2-rank/tree/main/external/discord

## Commands
The plugin includes the following commands:
- `!rankh` - Display available commands.
- `!rankannouce` - Allows players to disable/enable points annoucement.
- `!rank` - Allows players to check their current rank and points.
- `!stats` - Displays players statistics.
- `!top` - Display the top-ranked players.
- `!resetrank` - Resets a player's rank and points.
- `!ranksession` - Displays rank for the current map.
- `!topsessions` - Displays players statistics for the current map;
- `!statssessions` - Displays players statistics from for current map.

## Configuration
The plugin offers a configuration file that allows you to customize its behavior according to your server's requirements. You can modify settings such as points gained or deducted for different actions and other gameplay-related parameters.

Moreover, support translation and colors !

- Points file: `addons/vgrank/configs/points.cfg`
- Translations file : `addons/vgrank/configs/phrases.cfg`
- Core file : `addons/vgrank/configs/core.cfg`
