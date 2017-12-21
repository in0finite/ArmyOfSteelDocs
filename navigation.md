
how to solve problem with blocking agents ?

- make trees static parts of navigation : they will never be destroyed => will have infinite amount of resource - can be easily done => they can be baked together with terrain

- make trees static parts of navigation, but update navmesh when tree gets destroyed ; navmesh can be updated asynchronously, and only changed tiles will get updated, but will it be fast enough ?

- or just use small number of trees, hills, etc... anything that complicates navmesh ; increase voxel size (drastically reduces num triangles in a navmesh) ; each map can have around 20 trees (they will have large amount of wood, or perhaps infinite amount)

why forest, when we can just use trees ? - no single reason

perhaps a water is causing performance drop ? it's large, and it's part of navmesh, even through it's not walkable

