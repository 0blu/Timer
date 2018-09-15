# [Unsupported] Please look for another version

## Installation

1.) Download the plugin at https://github.com/0blu/Timer/releases

2.) Compiling
    2.1) Download at least Sourcemod v1.7 and extract it into your desktop.
    2.2) Goto addons/sourcemod/scripting/include and fill it with all files this timer provides from same folder.
    2.3) Drag and drop needed SP files onto spcomp.exe inside addons/sourcemod/scripting to compile them it should create all needed SMX files.

3.) Upload all SMX files, configs, sounds and materials onto your server.

4.) Insert "timer" keyvalue into configs/databases.cfg (no sqlite support).

5.) Change configs/timer/settings.cfg to your needs

6.) Change configs/timer/physics.cfg to your needs (the folder contains some example files for bhop, surf, etc.)

7.) Skip this part if you don't like to run Chatranks/Points ranking/Skillrank
    Depending on if you run a CS:GO or CS:S server, rename csgo-rankings.cfg/css-rankings.cfg to rankings.cfg (addons/sourcemod/configs/timer) to enable the ranking module.
    7.1) Compile simple-chatprocessor.sp  and upload it to your server to enable chatranks.

8.) Restart your server.

9.) Start creating zones or use included mappacks inside addons/sourcemod/gamedata/MySQL

## General Info

* Its a fork of https://github.com/zAfLu/Timer
* The parent fork is by https://github.com/Zipcore/Timer

* The plugin's code is based on Alongub's [Old Timer 1.0.7] (https://forums.alliedmods.net/showthread.php?t=189751).
* Timer 1.x and 2.0.x records can be converted for a donation, 
 * But it's better to start with a fresh database if you have used an older version as 2.1.3
* It is completely modular and extensible (private addons can be requested, just PN Zipcore).
* It measures the time, jumps, strafes,  etc. it takes players to finish the map.
* Players can choose their level of difficulty (style). (Each style is seperated by ranking, physics, etc.)
* You can create up to 32 styles and mix their settings with many [adjustments](https://github.com/0blu/Timer/blob/master/docs/modules/timer-physics.txt).
* It has an advanced world record system. There are also more advanceds stats available like playerinfo, latest records, etc.
* A map start and end is determined by map zones. You can add map zones in-game ([video (outdated)] (http://www.youtube.com/watch?v=YAX7FAF_N8Q)). 
* There are also glitch map zones, that try to stop players from exploiting map bugs that can possibly be used to cheat the timer (~ zones types).
* It has a customizable HUD that displays players their current timer and other info (or if you're a spectator it displays the timer of the player you're spectating).
* It has a Chatrank system which is based on a points-system.
* It supports only MySQL and is almost threaded to prevent laggs by your database.
* It supports CS:S and CS:GO (not all features are working on CS:GO).
* PHP-Stats to show top players/maps on your website
* You can also use custom sprites for zone beam effects ([video tutorial] (https://www.youtube.com/watch?v=uka1Iq_I6W4&feature=youtu.be)).
* There are also many other optional modules.

## Requirements
* CS:S or CS:GO gameserver
* MySQL database (SqLite isn't supported)
* MetaMod:Source & Sourcemod 1.7.x+
* Additional various requirements for some modules

## Compability Info

- Noblock (Included into Mapzone module)
- MultiPlayer Bunny Hops (Included into Physics module)
- Autobhop (Included into Physics module)
- Godmode (Build-in godmode into Physics module, with PvP Arena zone)
- SMAC autotrigger (Included into Scripter-SMAC module)
- Macrodox - Bhop cheat detection (Included into Scripter-Macrodox module)

## Usefull CVAR list

```
sv_accelerate_use_weapon_speed 0
sv_maxvelocity 350
sm_cvar sv_enablebunnyhopping 1
sv_staminajumpcost 0
sv_staminalandcost 0
sv_staminarecoveryrate 0
sv_airaccelerate 2000
sv_wateraccelerate 2000
```

## Problems?
* If you have still no clue you can ask for help [here] (https://github.com/0blu/Timer/issues/new).
