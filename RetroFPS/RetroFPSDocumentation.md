
## Welcome to the documentation for the Retro Graphics Template 🔲

This project is a great place to start if you're making a Lo-Fi, Retro, Pixelated, Early 3-D Style game.


## Important Tips

**Making a New Level**

To make retro features work properly, you will need to copy a set of actors from the RetroFPSTestMap into the new level.

"Lighting-Sky-PP" Folder contains all actors that need to be copied to each new level.

Lights are optional (DirectionalLight, PointLight, SkyLight) but recommended as a starting point.  
If you are making a dark level, consider using only Point Lights to illuminate it.

**Textures**

For crispy pixelation, please make sure your textures are set to "Filter: Nearest"

If you import many textures, I recommend selecting them all, right clicking, choose Assets Actions->Edit Selection in Property Matrix to assign all their Texture->Filter property at once.


## Where to Tweak Essential Settings
	
**FPS / Frame Rate**

	Project Settings -> Engine -> General Settings

If you don't use the fixed frame rate setting in Project Settings, I recommend setting a max frame rate.  
Console command "t.MaxFps 60" is useful for 60 (or any other) fps.

WARNING: The game runs super fast if you don't limit fps-- I was getting over 400 on my dev machine, causing high CPU usage.

**Resolution**

	/RetroFPS/Blueprints/BP_RetroFPS_GameState -> Fake Vertical Screen Resolution (float)


Note: To set the horizontal resolution, use Fake Vertical Screen Resolution in combination with changing the Aspect Ratio

**Aspect Ratio** 

	/RetroFPS/Blueprints/BP_RetroFPSCharacter -> FirstPersonCamera -> Camera Options & Camera Settings categories

**Pop-In / Distance Culling**

	Level Outliner -> Lighting-Sky-PP -> CullDistanceVolume

Adjust the properties on the cull distance volume, 
Or delete it to disable distance culling.
	
Documentation: https://dev.epicgames.com/documentation/en-us/unreal-engine/cull-distance-volumes-in-unreal-engine

**Distance Fog**

	/RetroFPS/Materials/PostProcesses/M_PP_DistanceFog

It has several parameters to adjust.
I recommend making Material Instances with different Parameters to adjust fog for different environs.  Adjust fog color, fog distance, fog depth e.g. Make one for Indoors, one for Outdoors.
	
To Apply / disable it in-level,

	Level Outliner -> Lighting-Sky-PP -> PostProcessVolume -> Rendering Features -> Post Process Materials

## Additional Note
Many project settings were changed to support this retro aesthetic.

Importing additional content will not break anything.  🎊

However, you cannot make an existing project match this Retro style by simply importing this project's contents.  You will also need to change various project settings to match this Retro project.

After all, that is why this project is a template instead of a plugin or content pack!

GLHF
