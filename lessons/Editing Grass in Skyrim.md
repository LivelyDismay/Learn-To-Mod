
# Editing grass in Skyrim

Alright, time to learn a little bit about editing grass and landscape. First thing, you should probably take a little bit of time to watch [this video](https://www.youtube.com/watch?v=q2Eisj7g3d8) by Darkfox127. I could probably not write much more because it’s a great video, and having never tried this before it got me basically through it. 

In Lexy’s guide, the start of M’rissi’s Tail of Trouble always causes problems for some folks. The problem is that S’ahara, the Khajiit that you save, tends to be hidden in the tall grass. People can’t find her and ask the same question in the help desks: “Where did she go?”

Well, she goes here. Hard to see, right?

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-1.png) 

As you can see the grass is pretty dense. We’re going to thin it out. First, let’s load everything in xEdit real quick and check out the M'rissi plugin. Find mrissitailoftroubles.esp and expand it.

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-2.png)

You can see that there are no landscape or grass records. That’s good, nothing to worry about there. So time to dive into the CK.

Open your Skryrim root folder and let’s make sure the creationkitprefs.ini has a few edits. Open it in your text editor of choice and search for [grass]. 

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-3.png)

You want to see bAllowCreateGrass=1 and bAllowLoadGrass=0. If you don’t see them, add them and save. Alternatively, you can add them to creationkitcustom.ini which is what I have done. These changes will ensure we can see the changes to grass in real-time in the CK.

After opening the CK, click Data... 

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-4.png)

Since nothing edits that landscape, let’s just check the master files and open the CK. We aren’t setting an active file because we want to save the output to a new plugin. 

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-5.png)

In the cell view, choose Tamriel.

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-6.png)

Then search for WhiterunWatchtowerExterior02. 

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-6.png)

Double click and wait for the render window to load.

As is typical, you start staring at the ground. Hold down Control and pan around until you are looking north towards Whiterun. Navigate to the area of the red circle.

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-7.png)

Use the scroll wheel to zoom forward and hold down the space bar if you need to strafe. Once you find spot, press H to open the landscaping tab. I have circled the area that S'ahara hides at.

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-8.png)
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-9.png)

Press B to show the cell borders. You can see we aren’t in WhiterunWatchtowerExterior02 anymore, which is fine. Let’s control-right-click here to see what texture is being used. It’s LFieldGrass01, which you can see in the Landscape tab. Press I. You can now see all the quads of the cell. 

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-10.png)

You can only have 6 textures per quad, but fortunately, the NoGrass version of that texture is in each quad. Close the quad tab. In the landscape tab, choose LFieldGrass01NoGrass. Let's choose radius 1, and opacity 100. Now if you wanted, you can left click and drag to change the height of the landscape. We won’t do that. Instead we will right-click to paint on the existing landscape. How about something like this.

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-11.png)

You can see that by painting the NoGrass texture, there is no more grass. Good stuff.

Now close the CK, choose save, and let's name this No Grass.esp. It will be saved into Overwrite. Make sure it is last in your load order and active, and then load up your game. At the main menu, console “coc WhiterunWatchtowerExterior02”. Let’s see how we did.

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-12.png)

Wait a second. Nothing changed. Why? Well, even though nothing was changing the landscape, our grass mod was still changing the textures. If you close Skyrim, disable Veydosbrom, and load back in you will see your change take effect. But we loaded our plugin last, why wasn’t it taking effect before?

Let’s load xEdit, and look at Veydosbrom.esp. Under Landscape Texture look for LFieldGrass01 and LfieldGrass01NoGrass. You can start to see what is happening. First, Veydosbrom breaks the world into Regions which have different types of grass, so each region has a more unique look. So even though our landscape has LFieldGrass01NoGrass as the texture, the texture set that is being used has different models and textures. Let's look in a bit more detail.

Here's the LFieldGrass01 record. 

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-13.png)

You can see that it uses a blend of grasses. The vanilla record uses a blend of two types of grass (TundraGrass 01 and 04). The Veydosbrom grass uses a blend of 8 types of grass. 

Here's the record for LFieldGrass01NoGrass. 

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-14.png)

Wait a second! It adds a bunch of grasses! That's annoying. Let's compare those two records. Click one of them in the left pane, then hold Control and click the other. 

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-15.png)

It seems they use the same types of grasses. The order doesn't matter.

Let's look a little deeper. Let's compare the Flower_06 type of grass between the two versions. 

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-16.png)

What's the difference here? The no grass version can grow on steeper slopes. Interesting choice, but at least we know what it's doing with that. Let's look at another. 

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-17.png)

Here's the tundra grass differences. In the NoGrass version, it is less dense, can grow on steeper hills, takes up less average space (that's the position range) and waves faster in the wind. Often these records are self explanatory, but if you don't know what they mean, go read [The Creation Kit wiki](https://www.creationkit.com).

If you want to dive even deeper, take a look at the texture set itself. You can see that each of those grasses constitute an alpha layer on the terrain, and have different opacities, which creates the blend of grasses that you see.

So how do we fix this. Let’s reload the CK, but this time load Veydosbrom.esp. Don’t set an active file. Find the same location.

Now we can see the space with textures more representative of we would see in our full game. Control click on a few different places to see what textures are there. This is where you get to experiment with what you think looks best. Paint something, save and check it in game. Try again.

First I tried with Tundra01. 

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-18.png)

Still too much grass in my opinion. What I ultimately did was right-click this area with zero grass. 

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-19.png)

TundraRocks01. Then I painted until I was happy. I saved it as Rocks.esp. Here it is in game with S’ahara. 

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/WT-Grass-20.png)

Now she is much more visible. Once I knew I was happy with how it looked, I went back into xEdit, made sure there were no unexpected edits. Then I flagged the plugin as ESL, saved it, and sent it to Lexy to roll into the main CR (conflict resolution) file. Enjoy mowing the lawns of Skyrim!
