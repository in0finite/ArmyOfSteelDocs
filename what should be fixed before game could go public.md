
- multiplayer : we need a server - or use matchmaking ; **use newer version of UnityEngine.Networking.dll and other networking dlls** - there are a couple of fixes for small irritating bugs ;

- default quality setting is not "recommended"

</br>

***
</br>

- use batch build when building for all platforms ? - it's too slow

- navigation : remove (or disable) NavMeshObstacle from tree - because it will be static part of navmesh

- AIGatherAction.cs:441 - null ex

- test tree removal on client - it fails sometimes - test all maps ;

- scene changing is most problematic: client didn't detect when country changed for a player (for no apparent reason) ; but even high end games must disconnect player before changing scene !! - so, it's not that bad - before changing scene, tell players to reconnect after some time - if needed, their score will be stored on server, and will be restored when they reconnect ; so, the solution for now is: don't change the scene :D ;

- switch to new version of unity - they may have fixed networking - no they haven't :(

