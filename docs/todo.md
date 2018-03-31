
## TODO

<br>

Priority : **functional (gameplay) stuff**

<br>

### Active

better transform syncing over network

<br>

***

new gameplay stuff :

- robot - download it from asset store ; hitpoints 450 ; attack damage 50 ; speed 3 ; cost wood 120 gold 120 ; they will need some attack effects ; AI will use it in 10% of his army ;
- nuclear missile - fired from missile silo, and treated as projectile ; travels slow (10 m/s) ; expensive ; takes 2 min to build new one ; travels high in the sky ; big damage, big area ; AI will fire it against current attack target, or against strongest enemy object ;
- tomahawk missile - also fired from missile silo ? ; travels above the ground ; much faster than nuclear missile ; high damage, but small area ; can be fired every 1 min ; AI will fire it against what ? ;
- missile silo - building with 2 attacks (nuclear, tomahawk) ; auto attack will be disabled ; there will be option to choose current projectile ; cost: wood 300 gold 300 ; AI will try to build it only if he has fort ;

adapt for FoW : trees ? ; explosion ; water ? ; building placement ; resource gatherer ; AI ; range ring ;

when owning object is attacked – play alert sound

minimap – add ability to draw circles ; take a picture of terrain to use as a background (from code, or maybe not) ;

Cursor – **texture is not updated until mouse is moved**

FoW – generate the texture by rendering to it – it will offload the work from CPU, and there won't be copying of texture to GPU - should greatly improve performance, especially for large maps

use line renderer for range ring ?

resources don't draw selection bar - Selectable should register itself with RTSGameManager to draw gui when it is selected

when to use circle search through cells : resource gatherer – when searching for resources ; AI gather action – when searching for resource ; AI – finding attack target ;

rocket launcher – create explosion on rocket impact ;

projectiles should be pooled

AI : **defend action** – it will also influence general AI behaviour ; maybe refresh grouping position over time ? ; join units even if grouping ; better attack target finding ; training coeficients should be affected by current trainings ; better continuation of attack campaign – if strength of objects is sufficient, don't move them back to town center (or back to grouping position) – move them back only if failed to find appropriate attack target ;

***

we need some powerful UI dialogs/windows for controlling nation, diplomacy, resources, settlers, trainings, etc – TabbedView, Table ;

**UI table** – each entry can be created with custom function (allows to create button, dropdown, slider, etc) ; option to enable/disable scrolling – if disabled, all entries are shrinked to fit size ; prefab will contain vertical scroll view ; script will ask for horizontal layout group prefab (or maybe not), and generate them as needed ;

create script which will automatically setup uGameCore – allows to import new version of uGameCore - not needed, because we can copy prefabs

cell should keep a List of all units inside, not a hashtable – it's because remove and lookup operations are rare (only when unit moves from one cell to another), while iteration is very often

AI attack – check for 30 objects every time (in a coroutine) ; check areas around path for enemy objects – maybe AI should not search through objects, but through areas – use circle search – this avoids the need to check areas around path ;

each object should have it's icon – where to use it : training button, object name button, training queue, info area, 

***

**nav mesh blocks when there are many units attacking**

settler (gathering and constructing) failure handling -> **implement MoveToObject** ;

**dont clone the whole terrain game object, just clone terrain data and assign it**

camera frustrum is not visible when playing 1000x1000 map - it's because texture is too large (1000x1000), and when it is resized to the size of UI image, the lines of camera frustrum are lost

what should be done separately (when on dedicated server) : 

what is not synced over network : projectiles ? ; building crash pieces ? ; AI enabled state for non-controlled countries ;

what does not use corners of object (but only transform position) : scanning for objects ; fog of war ; cell manager ;

settler : **if settler can not gather for certain amount of time, then try to find another gatherable of that type -> increase unwanted factor for that gatherable instance** ; if settler can not get to building to construct it, for certain amount of time, abort ; both of these 2 features can be handled with single script ;

start game menu : choose : country color, amount of resources to generate (not needed for now), startup buildings ; we need listbox of countries ;

when 'battle' scene is loaded : generate resources (not needed for now, we can use fixed resources created in editor) ;

create more of smaller maps – it's boring when map is huge

**perhaps rotate units based on terrain (use terrain normal as up vector)**

spawning buildings on scene startup : generate more spawn points (another circle) ; maybe we shouldn't pick spawn point with smallest sum of distances, but with highest distance to closest used position ;

tank is **too graphically demanding**

**nations' UI** – num idle settlers (constructed building is not synced -> wrong number of idle settlers) ; num settlers per resource ;

**objects' UI** : country flag ; goto button ; experience ; num kills ; object's icon ; training queue should be displayed using buttons ;

Prevent camera from going below water.

mobile : how to rotate (and even place ?) buildings on mobile ? - use mobile control rig ;  how to limit fps ;

speed up camera and zoom with shift 

**green selection box**

Objects can be selected even if under terrain.

Convert wall to gate.

Queued orders.

Spawning units – we need to sample nav mesh position ?

<br>

