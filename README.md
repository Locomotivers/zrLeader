# Zombie Reloaded Leader Plugin

The full credit goes to original author antiteal (and will leave sm forum post/link down). He didn't had repo to fork it!



[[ZR] Leader](https://forums.alliedmods.net/showthread.php?p=2559021)

#### Description
Allows for an admin to select or for regular players to vote for a human to be the leader for the current round. The leader gets special perks, like the ability to put defend here / follow me sprites above their head, place defend markers, toggle a rainbow beacon, custom chat, custom radio commands, and maybe more in the future.

### Requirements
This plugin requires Zombie:Reloaded.

#### Server ConVars
sm_leader_version - Leader Version (2.9)
sm_leader_allow_votes - Determines whether players can vote for leaders. (Default: "1")
sm_leader_defend_vmt - The defend here .vmt file (Default: "materials/sg/sgdefend.vmt")
sm_leader_defend_vtf - The defend here .vtf file (Default: "materials/sg/sgdefend.vtf")
sm_leader_follow_vmt - The follow me .vmt file (Default: "materials/sg/sgfollow.vtf")
sm_leader_follow_vtf - The follow me .vtf file (Default: "materials/sg/sgfollow.vtf")

#### Commands
sm_leader - Access the leader menu OR Set a player to be leader (ADMFLAG_GENERIC)
sm_currentleader - Shows the current leader.
sm_voteleader <player> - Votes for the specified player to be leader. Required votes is current player count / 10.
sm_removeleader (ADMFLAG_GENERIC) - Removes the current leader.

#### Planned Features
Config
More extensive API
More rainbow stuff

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


