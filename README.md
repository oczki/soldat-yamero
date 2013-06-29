#Yamero!

Yamero is a Soldat script for public servers. It punishes players for excessive spawnkilling, camping, and gets rid of players that occupy slot doing nothing (that is, being away from keyboard).

It won't work unless there are a few players, so AFKers won't get kicked unless the server is almost full. You can customize the thresholds though, so if you want, you can make Yamero kick campers after three seconds of staying still. That's for you to decide.

Players will get a warning first, then get killed remotely, and finally kicked out of the server. If you wany, it can ban them for a few minutes after kicking them out.

It works out of the box, but if you want to change some things, read on.

##Configuration
**MinPlayers_Spawn** (default: 6) - anti-spawn will work if there are at least X players. setting it lower than 6 makes no real sense  
**MinPlayers_Camp** (8) - anti-camp will work if there are at least X players  
**MinPlayers_AFK** (12) - as above, but for anti-AFK. recommended value: your player slots limit
	
**Spawn_Warn** (5) - spawnkill counter. a kill counts as a spawnkill if the victim lived for less than three seconds  
**Spawn_Kill** (9)  
**Spawn_Kick** (13)

**Camp_Warn** (12) - camping "ticks". a tick is counted every three seconds, so 10 ticks = 30 seconds of camping  
**Camp_Kill** (20)  
**Camp_Kick** (35)

**AFK_Time** (60) - seconds of not moving, counted only if near spawn point. up to 255 (max byte value)  
**AFK_Spec** (false) - _true_ - moves the player to spectator team. _false_ - kicks him out

**BanDuration** (3) - minutes; set 0 to kick only

##Other things worth mentioning

After each map, the user's "bad points" are reset to 0.

Player is marked as AFK if he is _on_, or _directly under_ his team's spawn point. If he moves from that point, his AFK counter is immediately reset.
