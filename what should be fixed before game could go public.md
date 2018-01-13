
- multiplayer : better transform updating (use photon networking ? **use lerping with Transform syncing ?**) ; we need a server - or use matchmaking ;

- build and publish (for linux and windows) - use batch build ?

- **remove "server_cmd" command** , add "clear" command

- **replace (or find free) third party models, textures, sounds**

***

- navigation : remove (or disable) NavMeshObstacle from tree - because it will be static part of navmesh

- AIGatherAction.cs:441 - null ex

- test tree removal on client - it fails sometimes - test all maps ;

- scene changing is most problematic: client didn't detect when country changed for a player (for no apparent reason) ; but even high end games must disconnect player before changing scene !! - so, it's not that bad - before changing scene, tell players to reconnect after some time - if needed, their score will be stored on server, and will be restored when they reconnect ; so, the solution for now is: don't change the scene :D ;

- switch to new version of unity - they may have fixed networking - no they haven't :(

