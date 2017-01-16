#Instructions
###How to install
1. Download hungergames.jar
2. Put hungergames.jar in your Bukkit/Spigot servers plugin folder
3. Start the server then stop it to generate the config file

###How to configure
1. Allowed Worlds: *worlds the player can join the game from*
  1. open config.yaml and look for **Allowed Worlds: {}** then add the lobby worlds to this list
  2. This can also be done with a command in game **`/hg addworld <worldname>`**
2. Return World: *the world players are put after they leave the game*
  1. open config.yaml and look for **Return World:** then add the world to this list
  2. This can also be done with a command in game **`/hg setreturn <worldname>`**
  3. You can also set the value to same, which returns them to the location where they joined from
  
###Permissions
####Parents:
  `hg.*` - *gives access to every command in the plugin,* **WARNING OWNER ONLY!!!**
  <br>
  `hg.default` - *gives access to join, play, invinte, vote to start, and leave the arenas*
  <br>
  `hg.admin` - *gives the ability to kick players from the arena, and to start the arena, inherits hg.default*
###Commands:

| Command   | Permission | Parent | Description |
|:-------:  |:----------:|:------:|:-----------:|
|`/hg help` |`hg.help`|`hg.default` `hg.*`|*gives a list of commands and how to use them.*|
|`/hg join <arena>` |`hg.join`|`hg.default` `hg.*`|*joins the specified arena.*|
|`/hg leave`|`hg.leave`|`hg.default` `hg.*`|*leaves the current game.*|
|`/hg invite <player>`|`hg.invite`|`hg.default` `hg.*`|*invites the specified player to the game you are in*|
|`/hg admin <player>`|`hg.admin`|`hg.admin` `hg.*`|*gives the player access to developer/admin commands.*|
|`/hg start <arena>`|`hg.start`|`hg.admin` `hg.*`|*a dev command that is used to force start a specific arena/game.*|
|`/hg setpos <arena> <number>`|`hg.setpos`|`hg.admin` `hg.*`|*a admin command that sets a possible spawing position where the player is to the specified arena.*|
|`/hg delpos <arena> <number>`|`hg.delpos`|`hg.admin` `hg.*`|*removes the specified point from the specified arena*|
|`/hg setloc <number: 1-2>`|`hg.setloc`|`hg.admin` `hg.*`|*a dev command that is used to set the bounds for adding chests.*|
|`/hg addchests <arena>`|`hg.addchests`|`hg.admin` `hg.*`|*adds the chests within the bounds to the specified arena*|
|`/hg delchests <arena>`|`hg.delchests`|`hg.admin` `hg.*`|*removes all chests from the specified arena*|
