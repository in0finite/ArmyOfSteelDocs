
- multiplayer : **test** ; better transform updating (use photon networking ? use lerping with Transform syncing ?) ; we need a server - or use matchmaking ;

- build and publish (for linux and windows)

- navigation : astar asset is useless without local avoidance - maybe find some script on net which can do it ? ; should tree have a NavMeshObstacle ? - no

- spectator UI is showing up on server ; some objects are not destroyed on client ; rockets don't move with gravity on clients ; projectiles dont move on client ; test tree removal on client - it fails sometimes ;

- scene changing is most problematic: client didn't detect when country changed for a player (for no apparent reason) ; but even high end games must disconnect player before changing scene !! - so, it's not that bad - before changing scene, tell players to reconnect after some time - if needed, their score will be stored on server, and will be restored when they reconnect ;

- switch to new version of unity - they may have fixed networking - no they haven't :(

