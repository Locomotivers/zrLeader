# Zombie Reloaded Leader Plugin [![Build Status](https://travis-ci.com/Locomotivers/zrLeader.svg?branch=master)](https://travis-ci.com/Locomotivers/zrLeader)

The full credit goes to original author [**antiteal**](https://forums.alliedmods.net/member.php?u=263656) (and will leave sm forum post link down below). He didn't had repo to me fork it!



[[ZR] Leader](https://forums.alliedmods.net/showthread.php?p=2559021)

#### Description
Allows for an admin to select or for regular players to vote for a human to be the leader for the current round. The leader gets special perks, like the ability to put defend here / follow me sprites above their head, place defend markers, toggle a rainbow beacon, custom chat, custom radio commands, and maybe more in the future.

### Requirements
This plugin requires Zombie:Reloaded.

#### Server ConVars
* sm_leader_version - Leader Version (2.11.5)
* sm_leader_allow_votes - Determines whether players can vote for leaders. (Default: "1")
* sm_leader_spawn_rad - Determines radius of spawn marker. **Do not go over 400 units or more!** (Default: "150.00") 
* sm_leader_marker_time_limit - Determines how long of spawn marker ring spawn into the field. **advise not to set timer higher since there is no other way to remove the ring besides wait** (Default: "40.0")
* sm_leader_marker_width - Determines width of outer ring. **Do not go over 10 units or ring gets trippy!** (Default: "3.5")
* sm_leader_marker_color - Determines color of spawn marker ring. There is failsafe in place and will default to red color with 100% opacity. (Default: "255,0,0,255")
* sm_leader_defend_vmt - The defend here .vmt file (Default: "materials/sg/sgdefend.vmt")
* sm_leader_defend_vtf - The defend here .vtf file (Default: "materials/sg/sgdefend.vtf")
* sm_leader_follow_vmt - The follow me .vmt file (Default: "materials/sg/sgfollow.vtf")
* sm_leader_follow_vtf - The follow me .vtf file (Default: "materials/sg/sgfollow.vtf")
* sm_leader_spawn_vmt - The spawn marker .vmt file (Default: "materials/sg/sgdefend.vmt")
* sm_leader_spawn_vmf - The spawn marker .vmf file (Default: "materials/sg/sgdefend.vmf")

#### Commands
* sm_leader - Set a player to be leader (ADMFLAG_GENERIC)
* sm_currentleader - Shows the current leader.
* sm_voteleader <player> - Votes for the specified player to be leader. Required votes is current player count / 10.
* sm_removeleader (ADMFLAG_GENERIC) - Removes the current leader.
* sm_lmenu - Opens up leader menu for current leader.
* sm_mark - Marks where the player is looking at
* sm_marker - Removes all marker
**You can only spawn one of these markers one at a time**
* +spawn - Places a spawn marker and ring where player is aiming at 
* -spawn - Removes all marker from leader player.
* sm_resignleader - Allows leader to resign from leader.

#### Planned Features
* Floor and Wall detection for spawn marker.

#### API
```sourcepawn
#if defined _leader_included_ 
  #endinput 
#endif 
#define _leader_included_ 

/** 
 * Returns current leader 
 * 
 * @return int    Client index of the leader (-1 = null) 
 */ 
native Leader_CurrentLeader(); 
/** 
 * Sets the leader 
 * 
 * @param client    Client index to be set as leader 
 */ 
native Leader_SetLeader(client);  
```

#### Screenshots
![](https://forums.alliedmods.net/image-proxy/ee3ad062a96a4c2c482aec2ee30ae56ce001dfe4/68747470733a2f2f737465616d75736572696d616765732d612e616b616d616968642e6e65742f7567632f3836323836343234363636363839373637362f353438323732313944443834463045393830454531303041344631434332434141324145303031432f)

![](https://forums.alliedmods.net/image-proxy/3beac2771cba4e625a33b339de5ae6a8a9ff1137/68747470733a2f2f737465616d75736572696d616765732d612e616b616d616968642e6e65742f7567632f3836323836343234363636363839373536352f393535324646354543453141414643363233443844444631363530353734323735383041454432332f)


