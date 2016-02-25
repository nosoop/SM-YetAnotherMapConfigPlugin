# Yet Another Map Config Plugin
Another plugin for running map-specific configuration files.  Huzzah.

## What makes this one special?
* Much like [Extended Map Configs][emc], it puts them all in an organized directory structure.  However, it doesn't autogenerate new / empty configuration files.
* Much like [CP Push and Attack / Defend Configs][cpcfg], this plugin can peek into the current running map and determine a specific subtype of game mode.
* Much like [Map Configs with Prefix Support][mcps], besides the full name, maps can be refered to by its prefix with trailing underscore.
* And like none of those plugins, this one also runs config files that match Workshop IDs.

[emc]: https://forums.alliedmods.net/showthread.php?p=760501
[cpcfg]: https://forums.alliedmods.net/showthread.php?p=913024
[mcps]: https://forums.alliedmods.net/showthread.php?p=607079

## About the directory structure
* `mapconfigs/` is a directory under the game's default `cfg` directory, similar to Extended Map Configs.  It contains the following:
  * `all.cfg`, which is executed for every map before map-specific configs.
  * `gametype/`, which contains configuration files based on map prefixes.  Some game modes have supported subtypes (e.g., TF2's Control Point game mode, split into Attack / Defend and Push variations).  More coming soon, maybe.
  * `maps/`, which contain map-specific configs.  Prefix support is provided.
  * `workshop/`, for maps from the Steam Community Workshop.  These can be refered to by Workshop ID (e.g., `619869471.cfg`).
