Dungeon Builders
================
The Default dungeon builder used to create the layout is swappable and you can provide your own implementation

![The Dungeon Builder can be swapped with your own implementation](../assets/images/da_design_builder.png)


This is useful if you want to use your own algorithm for generating the layout of your dungeons.  

You are not limited to a grid based system.  


Creating a new Builder
----------------------

To create a new builder, subclass `DungeonBuilder` under the `DungeonArchitect` namespace and implement the virtual methods

```
using UnityEngine;
using System.Collections;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using DungeonArchitect.Utils;

[ExecuteInEditMode]
public class MyDungeonBuilder : DungeonBuilder
{

    public override void BuildDungeon(DungeonConfig config, DungeonModel model) {
		base.BuildDungeon(config, model);

		// Add your builder logic here
    }


    public override void EmitMarkers() {
		base.EmitMarkers();

		// Emit markers here by calling EmitMarker()
	}
}

```

Have a look at `GridDungeonBuilder` under `Assets/DungeonArchitect/Scripts/Builders/GridDungeonBuilder.cs` for reference


Using a different Builder
-------------------------

If you've created a builder and would like to use it with your dungeon actor, drop in an existing dungeon actor, remove the existing builder script and replace it with your own

![Dungeon builder script attached to the Dungeon game object](../assets/images/dungeon_builder.png)


Example Builders
----------------
Dungeon Architect comes with a sample builder named SimpleCity.   It could be used as a good reference for building your own builders

![Builder Code Location](../assets/images/builder_example_path.png)

![Builder Samples Location](../assets/images/builder_example_path2.png)


![Sample City Builder](../assets/images/builder_simple_city_04.jpg)

![Sample City Builder](../assets/images/builder_simple_city_01.jpg)

There are also examples on how this sample builder can be further extended by the users using Marker Emitters script.   It is used emit markers around the boundary of the city, so theme files can decorate them as strongholds

![Stronghold Wall Emitter](../assets/images/builder_simple_city_03.jpg)

![Stronghold Wall Emitter](../assets/images/builder_simple_city_02.jpg)



