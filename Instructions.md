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
  
###Commands
`/hg` - *is the main command, will tell you to use /hg help for more information.*
<br>
`/hg help` - *gives a list of commands and how to use them.*
<br>
`/hg admin <playername>` - *gives the player access to developer/admin commands.*
<br>
`/hg start <arena>` - *a dev command that is used to force start a specific arena/game.*
<br>
`/hg join <arena>` - *joins the specified arena.*
<br>
`/hg leave` - *leaves the current game.*
<br>
`/hg invite <player>` - *invites the specified player to the game you are in*
<br>
`/hg setpos <arena> <number>` - *a admin command that sets a possible spawing position where the player is to the specified arena.*
<br>
`/hg setloc <number: 1-2>` - *a dev command that is used to set the bounds for adding chests.*


###Permissions
####Master Perms:
  `hg.*` - *gives access to every command in the plugin,* **WARNING OWNER ONLY!!!**
  <br>
  `hg.default` - *gives access to join, play, invinte, vote to start, and leave the arenas*
  <br>
  `hg.admin` - *gives the ability to kick players from the arena, and to start the arena, inherits hg.default*
####Per Command:

| Command   | Permission | Parent            |
|:-------:  |:----------:|:------:           |
|`/hg help` |`hg.help`   |`hg.default` `hg.*`|
|`/hg start`|`hg.start`  |`hg.admin` `hg.*`  |
|`/hg join` |`hg.join`   |`hg.default` `hg.#`|

  `hg.help` - *gives access to* `/hg help`
  <br>
  `hg.start` - *gives access to* `/hg start <arena>`
  <br>
  `hg.join` - *gives access to* `/hg join <arena>`
  <br>
  `hg.leave` - *gives access to* `/hg leave`
  <br>
  `hg.setpos` - *gives access to* `/hg setpos <arena> <number>`
  <br>
  `hg.setloc` - *gives access to* `/hg setloc <number: 1-2>`
  <br>
  `hg.invite` - *gives access to* `/hg invite <player>`
