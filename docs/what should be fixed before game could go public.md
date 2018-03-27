
- multiplayer : we need a server - or use matchmaking ; use newer version of UnityEngine.Networking.dll and other networking dlls - there are a couple of fixes for small irritating bugs ;

- test : network position syncing ; on different systems (linux, windows) ; on remote computers ;

- **network transform interpolation** - tested - not good - try:
	- history based interpolation (there is PR on bitbucket repo) 
	- sync velocity (we would need to get current velocity of nav mesh agent)
	- disable navmesh agent on clients ?
	- or just tweak parameters in new NetworkTransform

- record gameplay video

</br>
***
</br>

- use batch build when building for all platforms ? - it's too slow

- navigation : remove (or disable) NavMeshObstacle from tree - because it will be static part of navmesh

- AIGatherAction.cs:441 - null ex

- test tree removal on client - it fails sometimes - test all maps ;

- scene changing is most problematic: client didn't detect when country changed for a player (for no apparent reason) ; but even high end games must disconnect player before changing scene !! - so, it's not that bad - before changing scene, tell players to reconnect after some time - if needed, their score will be stored on server, and will be restored when they reconnect ; so, the solution for now is: don't change the scene :D ;

- switch to new version of unity - they may have fixed networking - no they haven't :(

