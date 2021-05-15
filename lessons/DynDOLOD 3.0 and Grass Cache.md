# Althro's Guide to DynDOLOD 3.0 and Grass Lods for Skyrim SE

## Intro
So you’ve got your modlist all nice and ready and are now onto the process of creating lods for your game. But how do I do them, and what on earth is a grass cache?

Well, you’re in luck as this guide goes over how to do it. I’ll not be covering all the settings, rather just how to run it and what you’ll need to run it. This guide is also only for Mod Organizer 2 users. If you are new to MO2, Wartortle has created a guide that you can follow [here](https://github.com/LivelyDismay/Learn-To-Mod/blob/58b4e895fd7885a0bd703b3b86685961d479fd2e/lessons/Introduction%20to%20MO2.md)

## What you will need

Here is a list of things you will need. 

The latest [xLodGen and SSE Tamriel Extended.esm](https://stepmodifications.org/forum/topic/13451-xlodgen-terrain-lod-beta-81-for-fnv-fo3-fo4-fo4vr-tes5-sse-tes5vr-enderal-enderalse/)
[DynDOLOD 3.00](https://www.nexusmods.com/skyrimspecialedition/mods/32382)
[DynDOLOD 3.00 Reources](https://www.nexusmods.com/skyrimspecialedition/mods/32382)
[No Grass In Objects](https://www.nexusmods.com/skyrimspecialedition/mods/42161) [only needed if doing grass lods. You need the ini and the MO2 precahce plugin]
[Landscape Fixes for Grass Mods](https://www.nexusmods.com/skyrimspecialedition/mods/9005) [optional but needed if doing grass cache]

## The Main Steps

### Installing Everything
xLodGen and DynDOLOD should be installed to the tools folder of wherever your Mod Organizer is. In my case it’s Tinvaak/Tools. Once they are there, open your Mod Organizer. Create new mods named “xLodGen Output”, “Grass Cache”, “TexGen Output”, “DynDOLOD Output” and “Occlusion Output”.  Add the x64 versions of xLodGen, TexGen and DynDOLOD as executables. We use the x64 as we are modding Skyrim SE and it is a 64 bit game. Note: You must add “-sse” to the arguments section for xLodGenx64, TexGenx64 and DynDOLODx64 otherwise they will fail to run. 

In the section where it says “create files in mod instead of overwrite” for xLodgen and Occlusion, set them to the mods of the names you just created (xLodgen Output and Occlusion Output respectively). I highly recommend having both 2 xLodGen’s, one named xLodgen and the other named occlusion. It just makes the process much quicker as you don’t have to change where the data goes. The arguments should look something like this:
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/DynDOLODAndGrass1.jpg)

For the No Grass in Objects pre-cacher, place the plugin in the “plugins” folder of where your mod organizer 2 is installed. Relaunch MO2 and it will appear in the tools area (Shown as a spanner and screwdriver).

Install DynDOLOD 3.0 resources, checking all of the options aside from “Low-Res LOD Textures” and “Holy Cow”. You can use the Low-Res LOD if you wish, but I think it’s best not to. Once you have it installed, you want it placed relatively high in your left pane. I have it positioned in the following location: 
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/DynDOLODAndGrass2.jpg)

Finally, you’ll want to install the SSE Terrain Tamriel extended esm. This is only needed during xLodGen and can be placed anywhere in the left pane of MO2. I tend to place it above the xLodGen Output. Once installed, activate it only when doing xLodGen and place it below the last worldspace ESM in your load order. In my case, this is Wyrmstooth.

### xLodGen
Once you have all of that installed, the output paths set, activate SSE Terrain Tamriel Extended and move it to the correct position in the right pane as mentioned in the previous section. If you are using “A Quality world map”, move that very high up in your mod organizer 2. I tend to move it and place it under DynDOLOD resources which should be one of the first mods in your left pane, as shown in the previous picture. Note: Some mods such as Majestic Mountains and Cathedral Landscapes come with files for Lod Generation. You will want to have these files activated during the process of running xLodGen. Majestic Mountains Lods in particular need to be active all the way through until Occlusion generation.

Then select xLodGenx64 from the drop down executables and press “Run”. It will proceed to load your entire load order and once done a Dialogue box will open similar to the following:
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/DynDOLODAndGrass3.jpg)

Right click in the worldspaces area and press “select all”. Ensure that only Terrain Lod is selected and then apply your Lod settings. I use the Lexy LOTD lod gen settings which can be [found here](https://lexyslotd.com/guide/finishing-line/#xlodgen). They provide the best balance of quality to performance. Allow it to run and do it’s work. Once done it will say “Lod Generation completed”. You can then close the program. Refresh mod organizer by pressing F5 and activate your xLodGen output. Deactivate SSE Terrain Tamriel and any other mods that you activated for the xLodGen process.

### Grass Cache (Optional)
Once you have completed xLodGen, it’s now time for Grass Cache. Grass cache is a relatively new technology that allows you to pre-cache grass for all worldspaces in the game. This allows for DynDOLOD to create grass lods to increase the distance which you can see grass and also can give a stabler experience. **Do Note this can cost performance if set incorrectly**. Before running grass cache, go into your No Grass In Objects mod, open the INI file and change the following lines to read the following:

`UseGrassCache` = True
`OverwriteGrassDistance` = 12000
`OverwriteGrassFadeRange` = 8000
`OnlyLoadFromCache` = True
`SkipPregenerateWorldSpaces` = "DLC2ApocryphaWorld;DLC01Boneyard;WindhelmPitWorldspace;DLC1ForebearsHoldout;DLC1VampireCastleCourtyard;WhiterunWorld;CWSiegeTestWorld;TestDLC1PlantWorld;TestMeganWorld;TestSnow;JaphetsFollyWorld;FXLightWorldSpace;KarthspireRedoubtWorld;FallowstoneCaveWorldStart;LabyrinthianWorld03;ShadowgreenCavernWorld;CWTestHold;3DNPCGabaniasWorld;SnowThroatWorld;TOKMountainPassWorld;zAoMVigilantWorld;zAoMWitchWorld;zCHColosseumWorld;zCHWasteland;zCHWhaleGraceyardWorld;zCOCursedWorld"
`DynDOLODGrassMode` = 1

A note on these settings. To improve performance, you can set the `OverWriteGrassDistance` and `OverwriteGrassFadeRange` to be lower. For the former, a setting of 8000 is a bit more than vanilla and may improve your performance. If you just wish to cache the grass but not for DynDOLDOD, change the `DynDOLODGrassMode` back to "=0". `SuperDenseMode` is another section that you can alter if you wish to tone down the grass amount. I leave this set at 7 as it gives a good balance of performance to visuals, however setting this to 6 can help improve performance.

Once you have set those settings, save the file and close it. Go back into MO2, go to the spanner and screwdriver icon, click on it, and then press “PreCache Grass”. A pop up will appear confirming that you wish to do this. Press Yes. Go grab a coffee and a good book or magazine as depending on your system, this can take a very long time.

Once it is completed, a pop up will appear saying that grass generation has been completed. **If you do not have a mod set to catch files generated during gameplay, the grass will be in the overwrite mod at the bottom of your mod oragnizer.** You should see a folder called “grass” with a load of .cgd files in it. Move that folder to the mod called “grass cache” that you created. Press F5 to refresh MO2 and then activate the mod.

### TexGen
Activate the TexGen Output mod in your MO2 left pane and run TexGenx64. Allow the tool to load your mods and then choose the following settings. **If you are not doing grass Lods: untick the grass checkbox.** Note the output path as to where TexGen is sending the output.
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/DynDOLODAndGrass4.jpg)

Press Start and allow the tool to generate the textures. Once done, the tool will open a pop-up. Press exit. Open the folder where the TexGen output is and copy it across to your TexGen Output mod. Press F5 to refresh mod organizer and then activate it.

### DynDOLOD

#### Enabling Grass Cache for DynDOLOD
To enable grass cache, you need to edit a line in the DynDOLOD_SSE.ini file. Navigate to where your DynDOLOD is located, open up the Edit Scripts folder and then the DynDOLOD folder. Open the DynDOLOD_SSE.ini file and change the following lines:
`Wizard`=0
`Grass`=1
`TerrainUnderside`=1 (This is only necessary if you use a mod such as Dynamic Volumetric Lighting and Sun Shadows)

Save the .ini file and reopen MO2.

#### Generation
Ensure that your xLodGen, TexGen and Grass Cache (if using) is active. Run DynDOLODx64 and allow it to load all your mods. In the top left section where it lists worldspaces, right click and press select all. Load the relevant rules that you want, in this case we’ll load medium rules. Set your settings to be the same as this:
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/DynDOLODAndGrass5.jpg)

Another note on settings. Billboard brightness is one that you adjust if you find that your lods are too bright in game. I have this set lower due to some of the tree mods I use. Ultra trees generates 3D tree lod and can be performance intensive depending on the tree mods you use. Checking `Generate Tree Lod` will generate "Hybrid Lods" which are less performance intensive at the cost of a minor visual decrease in quality. If you have 4GB vram or less, I would recommend not doing Ultra Tree Lod. Anything above `1024` on tile size billboard is not recommended as you are past the threshold of visual quality to performance. And finally, the rules govern how DynDOLOD will generate things and at what quality. **Note**: Certain tree mods require specialised tree rules in order for them to render properly in the worldspace. Known mods that require them include: Myrkvior, Trees Addon SE and Skyrim Flora Overhaul. It is likely there are more tree mods that require special rules. 

Once you have configured the settings to how you wish, press the "OK" button and DynDOLOD will begin it's generation. This can take a very long time depending on how many worldspaces you have and your system specifications. DynDOLOD 3.0 is multi-threaded now so on machines with multiple cores, it may compelte quicker. Once it is completed, a pop up will appear. Press “Save and Exit”. Navigate to the output folder where DynDOLOD generated to and move the data into the mod you created called “DynDOLOD Output”. Press F5 to reload MO2 and then activate the mod. DynDOLOD esm should be moved to be the last esm after your worldspace mods. In my case, that is Wyrmstooth so I place it after Wyrmstooth.ESM. DynDOLOD.esp should be the last esp in your load order for now.

### Occlusion
If you have not set a duplicate xLodGen for occlusion, change the output directory to be “Occlusion Output” and then run xLodGenx64. Again, allow it to load all your mods and load the dialogue box. As before, right click in the section where all your worldspace mods are press select all. Check occlusion and set it to be similar to this:
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/DynDOLODAndGrass6.jpg)

Press Generate. **Note:** if you have done grass cache, this process can take a very long time and use a lot of system resources. Once it has completed, a message will display in the logs saying “Generation complete”. Close xLodGen, refresh MO2 and then check the Occlusion Output mod. Ensure that occlusion.esp is the last mod in your load order.

You’re all done. Go and enjoy your new and improved Skyrim :D
