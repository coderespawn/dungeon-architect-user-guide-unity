Volumes
=======

Dungeon Architect provides various volumes to help you influence your dungeon as per your requirements.

You can find the various volume prefabs under `Assets/DungeonArchtitect/Prefabs`

![Platform Volume Prefab](../assets/images/asset_prefab.png)

Platform Volume
---------------

Place a platform volume anywhere in the scene and Dungeon Architect would adjust the dungeon layout and create a platform (room or corridor) at that location.  Scale the volume along the XZ plane to change the size of the generated platform.   You can move the platform volume with the move tool to the desired location. (Rotation is not supported)

This gives you artistic control and lets you manipulate the dungeon to suit your needs

To place a platform volume,  navigate to `Assets/DungeonArchtitect/Prefabs`

![Platform Volume Prefab](../assets/images/volume_platform.png)

Drag and drop the Platform Volume Prefab into the scene view

![Platform Volume Prefab](../assets/images/pv01.jpg)

Select the platform volume and have a look at it's properties

![Platform Volume Properties](../assets/images/pv_prop.png)

The Volume needs to know which dungeon the volume belongs to (DA Supports mulitple dungeons within the same scene). 

Assign the dungeon you'd like this volume to affect in the **Dungeon** field

Select the type of cell to create on this platform's location (Room or Corridor)

Corridors form isolated platforms in the dungeon which merge nicely with existing corridor cells

![Corridor platform](../assets/images/pv02.jpg)

![Merges nicely with existing procedural layout](../assets/images/pv03.jpg)

![Volume moved up along the Y-axis](../assets/images/pv04.jpg)

![Volume moved down along the Y-axis](../assets/images/pv05.jpg)


Rooms always connect to atleast one other room in the dungeon.  Changing the Cell type to *Room* creates this result

![Room platform](../assets/images/pv06.jpg)

A button to rebuild the dungeon is provided for convenience.  It rebuilds the dungeon in the scene


Theme Override Volume
---------------------
Give certain areas of you dungeons a different look and feel.   Layout inside this volume would use the theme defined by this volume.  

This is useful for adding variations to your level

![Sample Dungeon](../assets/images/tov_01.jpg)

![Selective areas overriden by Theme Override Volumes](../assets/images/tov_02.jpg)

![Geometry within the volume picks up the theme defined by the volume](../assets/images/tov_03.jpg)

Select the theme override volume and have a look at it's properties

![Theme Override Volume Properties](../assets/images/tov_prop.png)

**Dungeon**: Set the dungeon game object this volume should affect

**Override Theme**: Set the dungeon theme asset you would like to apply to the geometry within this volume

Note: When overriding, the themes needs to be designed for the same grid cell size for proper results

A button to rebuild the dungeon is provided for convenience.  It rebuilds the dungeon in the scene


Negation Volume
---------------
This volume removes all procedural geometry inside of this volume.  Use this to get rid of procedural geometry in areas you do not need or when it is getting in the way while manually painting your layout

![Procedural geometry we'd like to remove](../assets/images/nv_01.jpg)

![Geometry inside the volume removed after a rebuild](../assets/images/nv_02.jpg)

Select the negation volume and have a look at it's properties

![Geometry inside the volume removed after a rebuild](../assets/images/nv_prop.png)

**Dungeon**: Set the dungeon game object this volume should affect

A button to rebuild the dungeon is provided for convenience.  It rebuilds the dungeon in the scene
