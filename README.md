BukkitSettings
==============

Plugin for handling a player's settings

This Fork
==============

This fork of BukkitSettings provides support for StruckBukkit (a private implementation of Bukkit created by the HungerStruck development team). StruckBukkit centralizes our redis connection pool, and this version of BukkitSettings will store settings data through redis for persistence across servers. 

If this plugin is used in a non-StruckBukkit environment, it will still function normally, and instead default to using metadata to store settings info. However, for non-redis supporting Bukkit implementations, please use @OvercastNetwork's [BukkitSettings plugin](https://github.com/OvercastNetwork/BukkitSettings).

Permissions
===========

`setting.list`

Allow the user to use the /settings command.  Defaults to true for everyone
unless otherwise specified.

`setting.<name>`

Allows the user to view, get, and set the setting identified by *name*.
Defaults to true for everyone unless otherwise specified.  Removing this
permission sets all child settings to false (can be overrided though).

`setting.<name>.view`

Allows the user to view the setting in all BukkitSettings commands.  Defaults
to true for everyone unless otherwise specified by a parent permission node or
otherwise.

`setting.<name>.get`

Allows the user to get the value of a setting.  Inherits value from parent
permission.

`setting.<name>.set`

Allows the user to set the value of a setting.  Inherits value from parent
permission.
