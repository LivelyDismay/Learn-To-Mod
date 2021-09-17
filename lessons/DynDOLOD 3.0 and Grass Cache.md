# DynDOLOD 3.0 and Grass Lods for Skyrim SE - by Althro

## Intro
So you’ve got your modlist all nice and ready and are now onto the process of creating lods for your game. But how do I do them, and what on earth is a grass cache?

Well, you’re in luck as this guide goes over how to do it. I’ll not be covering all the settings, rather just how to run it and what you’ll need to run it. This guide is also only for Mod Organizer 2 users. If you are new to MO2, Wartortle has created a guide that you can follow [here](https://github.com/LivelyDismay/Learn-To-Mod/blob/58b4e895fd7885a0bd703b3b86685961d479fd2e/lessons/Introduction%20to%20MO2.md).

## What you will need

Here is a list of things you will need: 

- The latest [xLodGen and SSE Tamriel Extended.esm](https://stepmodifications.org/forum/topic/13451-xlodgen-terrain-lod-beta-81-for-fnv-fo3-fo4-fo4vr-tes5-sse-tes5vr-enderal-enderalse/)  
- [DynDOLOD 3.00](https://www.nexusmods.com/skyrimspecialedition/mods/32382)  
- [DynDOLOD 3.00 Reources](https://www.nexusmods.com/skyrimspecialedition/mods/52897)  
- [No Grass In Objects](https://www.nexusmods.com/skyrimspecialedition/mods/42161) (only needed if doing grass lods. You need the ini and the MO2 precache plugin)  
- [Landscape Fixes for Grass Mods](https://www.nexusmods.com/skyrimspecialedition/mods/9005) (optional but needed if doing grass cache)
- [Worldspaces with Grass SSEEdit Script](https://www.nexusmods.com/skyrimspecialedition/mods/55152)  

## The Main Steps

### Installing Everything
xLodGen and DynDOLOD should be installed to the `tools` folder of wherever your Mod Organizer is. In my case, it’s `Tinvaak\Tools`. Once they are there, open your Mod Organizer. Create new mods named `xLodGen Output` and `Grass Cache`.  Add the x64 versions of xLodGen, TexGen and DynDOLOD as executables. We use the x64 as we are modding Skyrim SE and it is a 64-bit game. Note: You must add `-sse` to the arguments section for xLodGenx64, TexGenx64 and DynDOLODx64; otherwise they will fail to run. 

In the section where it says “create files in mod instead of overwrite” for xLodgen, set it to the mod of the name you just created (`xLodgen Output`). The arguments should look something like this:

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/DynDOLODAndGrass1.jpg)

For the No Grass in Objects pre-cacher, place the plugin in the `plugins` folder of where your Mod Organizer 2 is installed. Relaunch MO2 and it will appear in the tools area (Shown as a spanner and screwdriver).

Install DynDOLOD 3.0 resources, checking all of the options aside from “Low-Res LOD Textures” and “Holy Cow”. You can use the Low-Res LOD if you wish, but I think it’s best not to. Once you have it installed, you want it placed relatively high in your left pane. I have it positioned in the following location:

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/DynDOLODAndGrass2.jpg)

Finally, you’ll want to install the `SSE-Terrain-Tamriel Extended` ESM. This is only needed during xLodGen and can be placed anywhere in the left pane of MO2. I tend to place it above the xLodGen Output. Once installed, activate it only when doing xLodGen and place it below the last worldspace ESM in your load order. In my case, this is `Wyrmstooth`.
  -  *Note: Your ESMs will all be **bold** in MO2's Plugin list, even though they may not necessary be named with an `.esm` extension.*

### xLodGen
Once you have all of that installed and the output paths set, activate `SSE-Terrain-Tamriel Extended` and move it to the correct position in the right pane as mentioned in the previous section. If you are using `A Quality World Map`, move that very high up in your Mod Organizer 2. I tend to move it and place it under `DynDOLOD Resources`, which should be one of the first mods in your left pane, as shown in the previous picture.

  -  *Note: Some mods such as Majestic Mountains and Cathedral Landscapes come with files for Lod Generation. You will want to have these files activated during the process of running xLodGen. Majestic Mountains Lods in particular needs to be active all the way through until Occlusion generation.*

Then select xLodGenx64 from the executables dropdown in MO2 and press `Run`. It will proceed to load your entire load order. When it is done, a Dialogue box will open similar to the following:

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/DynDOLODAndGrass3.jpg)

Right click in the `Worldspace` area and press `Select All`. Ensure that only Terrain Lod is selected and then apply your Lod settings. I use the Lexy LOTD lodgen settings, [which can be found here](https://lexyslotd.com/guide/finishing-line/#xlodgen). They provide the best balance of quality and performance. Allow it to run and do its work. When complete, it will say “Lod Generation completed”. You can then close the program. Refresh Mod Organizer 2 by pressing `F5` and activate your xLodGen output. Deactivate `SSE-Terrain-Tamriel` and any other mods that you activated for the xLodGen process.

### Grass Cache (Optional)
Once you have completed xLodGen, it is now time for Grass Cache. Grass Cache is a relatively new technology that allows you to pre-cache grass for all worldspaces in the game. This allows for DynDOLOD to create grass lods to increase the distance which you can see grass and also can give a more stable experience. **Do Note this can hurt your performance if set incorrectly**. Before running grass cache, I recommend you use this script [here](https://www.nexusmods.com/skyrimspecialedition/mods/55152) to determine which locations to cache grass into. Download that script, save the zip file somewhere safe, and copy the file that ends ".pas" into your xEdit edit scripts folder as shown below:

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/DynDOLODAndGrass4.png)

Open xEdit, allow all your plugins to load, and then apply the script. This process can take a while so grab a coffee. Once completed, a textbox will show on screen with the list of worldspaces to generate grass for. 

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/DynDOLODAndGrass5.png)

Copy this data and thengGo into your `No Grass In Objects` mod, open the INI file, and paste the data in between the "" in the `OnlyPregenerateWorldSpaces =` section. It is **vital** this data is in between the quotes, otherwise it will not be read. You can see an example of how it should look below:

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/DynDOLODAndGrass6.png)

Staying in the ini file, change the following lines to read the following:

- `UseGrassCache = True`  
- `OverwriteGrassDistance = 12000`  
- `OverwriteGrassFadeRange = 8000`  
`OnlyLoadFromCache = True`  
- `DynDOLODGrassMode = 1`  

A note on these settings: to improve performance, you can set the `OverWriteGrassDistance` and `OverwriteGrassFadeRange` to be lower. For the former, a setting of 8000 is a bit more than vanilla and may improve your performance. If you just wish to cache the grass but not for DynDOLDOD, change the `DynDOLODGrassMode` back to `=0`. `SuperDenseMode` is another section that you can alter if you wish to tone down the grass amount. I leave this set at `7` as it gives a good balance of performance to visuals; however, setting this to `6` can help improve performance.

Once you have applied your settings, save the file and close it. Go back into MO2, click on the spanner and screwdriver icon, and then select `PreCache Grass`. A pop-up will appear confirming that you wish to do this. Click `Yes`. Go grab a coffee and a good book or magazine - this can take a very long time.

Once it is completed, a pop-up will appear saying that grass generation has been completed. **If you do not have a mod set to catch files generated during gameplay, the grass will be in the `overwrite` mod at the bottom of your Mod Oragnizer's left pane (assuming you have the mods sorted by `Priority`).** You should see a folder called `grass` with a load of `.cgd` files inside. Move that folder to the mod called `grass cache` that you created. Press `F5` to refresh MO2 and then activate the mod.

### TexGen
Run TexGenx64 and Allow the tool to load your mods and then choose the following settings. **If you are not doing grass lods, untick the grass checkbox.** Note the output path as to where TexGen is sending the output.

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/DynDOLODAndGrass7.png)

  -  *Note: Some grass mods do not have the bounds correctly set which can result in the grass not being genned correctly. To fix this, load your grass mod in the Creation Kit, go to the grass section, select all of the new grass, right click and press `recalculate bounds`. This will update the `OBND` data to properly reference the bounds of the mesh which will allow the lod to be generated correctly. Known grass mods that have this issue include Veydosebrom Regions, which requires the BSA unpacking to update. It is possible other mods also have this issue.*

Press `Start` and allow the tool to generate the textures. Once done, the tool will open a pop-up. Press `Exit` or `Zip&Exit` if you wish to have the output zipped up for easier addition to a mod-manager or redistribution. In this case, we're choosing `Zip&Exit` as that allows us to add the output as a new mod in MO2 easier.

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/DynDOLODAndGrass8.png)

Add the output as a new mod in Mod Organizer 2, and then activate it.

### DynDOLOD & Occlusion

#### Enabling advanced mode (Optional)

  - *Note: This portion isn't totally necessary as you can press the advanced button when DynDOLOD opens. I prefer to not have to press that button so set it in the ini file.*

If you want to have DynDOLOD start in advanced mode each time and not have to press the advanced button, you need to edit a line in the `DynDOLOD_SSE.ini` file. Navigate to where your DynDOLOD is located, open up the `Edit Scripts` folder, and then the DynDOLOD folder. Open the `DynDOLOD_SSE.ini` file and change the following lines:  
`Wizard=0`  

Save the .ini file and reopen MO2.

#### Generation

Ensure that your xLodGen, TexGen and Grass Cache (if using) is active. Run DynDOLODx64 and allow it to load all your mods. In the top left section where it lists worldspaces, right click and press select all. Load the relevant rules that you want, in this case we’ll load medium rules. Set your settings to be the same as this:

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/DynDOLODAndGrass9.png)

Another note on settings. Billboard brightness is one that you adjust if you find that your lods are too bright in game. I have this set lower due to some of the tree mods I use. Ultra trees generates 3D tree lod and can be performance-intensive depending on the tree mods you use. Checking `Generate Tree Lod` will generate "Hybrid Lods" which are less performance intensive at the cost of a minor visual decrease in quality. If you have 4GB vram or less, I would recommend not doing Ultra Tree Lod. Anything above `1024` on tile size billboard is not recommended as you are beyond the threshold of visual quality to performance. And finally, the rules govern how DynDOLOD will generate things and at what quality. 

  -  *Note: Certain tree mods require specialised tree rules in order for them to render properly in the worldspace. Known mods that require them include: Myrkvior, Trees Addon SE and Skyrim Flora Overhaul. It is likely there are more tree mods that require special rules.* 

If you wish to generate Grass cache, ensure that the grass lod option is enabled and that the mode is set to `1` as that was the mode that we used for grass generation. You can change the density if you wish, however I have left it as default.

  - *Note: This will not be active if DynDOLOD does not detect grass billboards.*

DynDOLOD 3.0 now includes Occlusion as part of it's toolset so we no longer need to generate Occlusion via xLodGen. I recommend the settings shown in picture above for generation as these are very similar to the original one's used in xLodGen occlusion.

Once you have configured the settings how you wish, click `OK` and DynDOLOD will begin its generation. This can take a very long time depending on how many worldspaces you have, as well as your system specifications. DynDOLOD 3.0 is multi-threaded now so on machines with multiple cores, it may complete faster than you think, if you've used DynDOLOD before. Once it is completed, a pop-up will appear. As with TexGen, you have the option to either `Save&Exit` or `Save&Zip&Exit`. Again, the choice is yours however in this guide we'll choose to zip it up as well.

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/DynDOLODAndGrass10.png)

Add the zipper output file as a new mod in MO2, name it `DynDOLOD Output` and activate the mod. On the right pane, `DynDOLOD.esm` should be moved to be the last ESM after your worldspace mods. In my case, that is Wyrmstooth so I place it after `Wyrmstooth.esm`. `DynDOLOD.esp` should be the second last and `Occlusion.esp` shoud be the last plugin in your load order.

You’re all done. Go and enjoy your new and improved Skyrim!
