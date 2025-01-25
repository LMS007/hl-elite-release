# Half-Life Elite Commands Manual Page

On this page you can find information about any added server or client commands. You can also find details about the accepted values and some examples. I will also include any changed commands.

- [Half-Life Elite Commands Manual Page](#half-life-elite-commands-manual-page)
- [Buttons](#buttons)
- [Client Commands](#client-commands)
- [Client Cvars](#client-cvars)
- [Server Commands](#server-commands)
- [Server Cvars](#server-cvars)

# Buttons
In this section I will give information about any new binds that can be used for activating special effects, as well as other possible (default) keys.

| Bind | Key | Comment/Example |
| --- | --- | --- |
| `+longjump` | `ANYKEY` | Longjump, much more accurate then a script |
| `playtrack` |`ANYKEY` | winamp play |
| `pausetrack` |`ANYKEY` | winamp pause
| `previoustrack` |`ANYKEY` | winamp previous track |
| `nexttrack` |`ANYKEY` | winamp next track |
| `stoptrack` |`ANYKEY` | winamp stop |
| `+volumedown` |`ANYKEY` | winamp volume up |
| `+volumeup` |`ANYKEY` | winamp volume up |

Example usage:

```
bind "Z" "+longjump" 
```

This will bind the long jump functionality to `Z` keyboard key. 


[Back To TOP](#half-life-elite-commands-manual-page)

# Client Commands

In this section you can learn about the client sided commands. Every player has access to those commands with no limitations.

| Command | Values | Comment/Example |
| --- | --- | --- |
| `help` | \- | opens help menu and list all commands and cvars |
| `menu` | \- | opens the vgui menu (bind this in the launch menu )|
| `drop` | \- | reviels a drop menu with drop commands, mp_tossitem must be set to 1 |
| `drop weapo`n | \- | shotcut to drop a weapon|
| `drop health` | \- | shotcut to drop a health kit |
| `drop battery` | \- | shotcut to drop a hev battery |
| `drop flag` | \- | shotcut to drop the flag |
| `drop ammo1` | \- | shotcut to drop primary ammo |
| `drop ammo2` | \- | shotcut to drop secondary ammo |
| `drop longjump` | \- | shotcut to drop the longjump |
| `vote` | \- | this is folowed by any command within the mp_validvotes string, example "vote mp_fraglimit 100, changelevel boot_camp". Two votes per line max seperated by a comma |
| `yes` | \- | vote yes |
| `no` | \- | vote no |
| `info` | \- | shows server cvar settings & player wonid's |
| `ms` | `0-3` | calls a vote for mastartstart # |
| `spectate` | \- | start observer |
| `-spectate` | \- | stop ovserver |
| `spec_mode` | `0-6` | changes spectator views |
| `follownext` | `0-32` | based on players |
|` taunt` | \- | taunt sound |
| `spawnme` | \- | add self to list, also this will automaticly vote yoursels into a match if it has started | 
| `add_flag` | \- |  places a flag in the level after a ctp file was opened, this will be saved to the file |
| `add_loc` | \- | places a location in the level after a loc file was opened, this will be saved to the file |
| `changeteam` | \- | changes team during a teamplay game, if a matchstart initiated, then a vote will automatically be called |
| `emitme` | \- | calls a vote to be emited into a match | 
| `ejectme` | \- | removes yourself from play queue during a round based mode, or removes yourself from a match after a matchstart |
| `vrcon` | `commands` | refer to vadmin in the help documentation |
| `vgroup` | `group name` | refer to vadmin in the help documentation |
| `vadministration` | `group name` | refer to vadmin in the help documentation |
| `vrcon_password` | `password` | refer to vadmin in the help documentation |


[Back To TOP](#half-life-elite-commands-manual-page)

# Client Cvars

In this section you can learn about the client sided cvars. Every player has access to those commands with no limitations.

| Command | Values | Comment/Example |
| --- | --- | --- |
| `hue` | `0-255` | hud color | 
| `value` | `0-1` | hud brightness |
| `gauss` | `0-8` | gauss color |
| `xhairs` | `name` | strings are determined by the folders names in the sprites/crosshair dir |
| `cl_showclock` | `0-1` |  turns on and off hud clock at bottom |
| `cl_showtimer` | `0-1` | turns on and off hud timer at top |
| `cl_showlock` | `0-1` | turns on and off hud lock |
| `cl_scrollspeed` | `*` | changes the map scroll speed, default `800` |
| `cl_dynamic_xhrs` | `0-1` | turns on and off crosshair colors |
| `cl_radar` |  | turns on and off client side radar |


[Back To TOP](#half-life-elite-commands-manual-page)

# Server Commands

In this section you can learn about the server sided commands. You have access to those if you’re hosting a dedicated server or you’re hosting a local game.

| Variable | Values | Comment/Example |
| --- | --- | --- |
| `matchstart` | 0-3 | 0 cancels, 1 starts unloaded, 2 starts loaded, 3 does not respawn players |
| `create_ctp_file` | | opens or overwrites a ctp file for a map and removes all flags in a level |
| `complete_ctp_file` |  | closes and locks the ctp file |
| `create_loc_file` |  | opens or overwrites a loc file for a map |
| `complete_loc_file` |  | closes and locks the loc file |
| `add` |  | refer to vadmin.txt |
| `remove` |  | refer to vadmin.txt |
| `emit` | `serverID#` `teamname`  | emits a player into the play queue for a round based mode, or emits a player into a match with the given team name if provided; example "emit 4 red" that will force the 4th player to spawn under the red team. to find the players serverID# number type "status" |
| `eject` | `serverID#` | this is the opposite of emit, it will force a player into spectator mode, thus removing him from the play queue or a match if started. To find a players serverID#, type "status"; example "eject 5" |
| `start` | string | string will be the name of your config file for a particualr tournament inside the tournament dir. This command starts the tourney |
| `action` |  | changes game mode; teamplay:NO, matchstart: NO |
| `duel` |  | changes game mode; teamplay:NO, matchstart: NO |
| `lms` |  | changes game mode; teamplay:NO, matchstart: NO |
| `tournament` |  | changes game mode; teamplay:NO, matchstart: NO |
| `lts` |  | changes game mode; teamplay:YES, matchstart: NO |
| `teamaction` |  | changes game mode; teamplay:YES, matchstart: NO |
| `ffa` |  | changes game mode; teamplay:NO, matchstart: YES |
| `teamplay` |  | changes game mode; teamplay:YES, matchstart: YES |
| `ctp` |  | changes game mode; teamplay:YES, matchstart: YES |
| `ctf` |  | changes game mode; teamplay:YES, matchstart: YES |
| `practice` |  | changes game mode; teamplay:NO, matchstart: NO |

[Back To TOP](#half-life-elite-commands-manual-page)

# Server Cvars

In this section you can learn about the server sided cvars. You have access to those if you’re hosting a dedicated server or you’re hosting a local game.

| Variable | Values | Comment/Example |
| --- | --- | --- |
| `nextmap`	| | overwrites mapcycle for the nextlevel, the nextlevel will be nextmap string |
| `mp_maxteams` | 2-6 | `#` of allowed teams, will work in this order: blue,red,green,yellow,purple,orange |
| `mp_flaghandicap` | 0-1 | `%` of gauss jump reduction when clients have flags in ctf mode |
| `mp_gamemode` | string | current gamemode |
| `mp_spawnlimit` | 0-* | for tourney mode only |
| `mp_bunnyhop` | 0-1 | turns on and off old school bunning hopping |
| `mp_autojump` | 0-1 | turns on autojump which allows players to jump over and over again by holding the jump button, this evens the playing field against bunny hop scripters |
| `mp_roundtime` | 0-*  | for duel/lms/tournament rounds, this appears at the top of the screen opposed to mp_timelimit which is at the bottom |
| `mp_winlimit` | 0-* | for ctf, lms, tournament and duel |
| `mp_spawnform` | 0-1 | 0 = start normal, 1 = start loaded |
| `mp_tossitem` | 0-1 | prevents droping items like the longjump |
| `mp_corpsequeue` | 0-* | # of dead bodies allowed at once |
| `mp_loselongjump` | 0-1 | Forces the longjump to fall off a player after he/she dies |
| `mp_showlongjump` | 0-1 | If on, this will hide the third person longjump on players backs, restart or changelevel required |
| `mp_satchelexplode` | 0-1 | If set to 1, this will allow other players to blow up your satchels with other explosives, this is used for CTF and CTP modes to prevent flag camping. |
| `mp_radar` | 0-1 | turns on and off the radar for all clients, restart or changelevel required |
| `mp_allowmatchvotes` | 0-1 | turns voting off during a match, in which case only a server admin can alter server settings |
| `mp_resumetime` | 0-* | number of seconds a player is allowed to join back into a match after a disconnect. The players score will be restored |
| `sv_banmodes` | string | ban all game modes you dont wish for clients to vote on |
| `sv_allowvotes` | 0-1 | enables/disables all voting |
| `sv_banentities` | string | ban weapons and entities here, if you only give part of the string, it bans every entity example "weapon_" bans every weapon |

[Back To TOP](#half-life-elite-commands-manual-page)

* * *
**Half-Life Elite SDK Documentation**

* * *
