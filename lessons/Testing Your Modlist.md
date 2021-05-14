# Testing Your Modlist

Before we get started here, it is important to start with a brief disclaimer: while this may be useful to anyone building a custom modlist, it is designed to help potential train and recruit modlist testers for Wabbajack modlist submissions. Anyone is free to give it a shot, and please let us know in the [Wabbajack Discord](https://discord.gg/wabbajack) if there's anything at all we can help you with.

You've downloaded and installed your mods. You patched everything you've seen that needs patching and addressed any potential issues. It's time for a final rundown.

This document will try to show you some proper steps when it comes to resolving any outstanding issues in any modlist, what to look for, how to fix issues, and all that fun stuff. A vast majority of our time will be spent in [xEdit](https://github.com/LivelyDismay/Learn-To-Mod/wiki/xEdit-Lessons).

Let's get started.

For the purposes of this exercise, I will be using the Magnum Opus modlist from Wabbajack.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6a2997d302c1b78584d07849b94e388866937bc1/images/testing1.png)

Here we've got a fully set-up portable instance of [Mod Organizer 2](https://github.com/LivelyDismay/Learn-To-Mod/blob/58b4e895fd7885a0bd703b3b86685961d479fd2e/lessons/Introduction%20to%20MO2.md). One of the first things you'll notice is the first separator at the top with a version number. While not *required*, this is very strongly encouraged. It can be a quick reference for users to know which version of a modlist they're playing (or which version you're testing).

Click the Plugin count on the right side. You'll see this little pop-up:  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6a2997d302c1b78584d07849b94e388866937bc1/images/testing2.png)

The most important part here is `ESMs+ESPs`. If this number is higher than 254, the list is broken.
  -  *Note that this only applies to Skyrim and Fallout 4. Other games, such as the older Fallouts, have smaller limits. Non-BGS games don't have any such limit.*
  -  *If testing a Skyrim: Legendary Edition or Skyrim/Fallout 4 VR modlist, ESL files are not supported.*

Next, scroll through the load order. There is no real need to scrutinize this too closely - most conflicts and issues will be resolved via patches toward the end. One thing I do like to look for, however, is the way the plugins are arranged. Many people rely solely on tools like LOOT, which has a...pretty obvious way of arranging plugins. Largely alphabetical, with patches loaded directly after the mod they're patching. A vast majority of modders that are sorting plugins by hand will load all the patches near the end, as this is a much easier way to keep track of your files.

Another thing to look for is a mod in the left pane with Cleaned DLCs. The name may vary depending on the mod author, but it should be rather obvious. You may notice Magnum Opus has no such mod - cleaning the DLCs is a much more important step for Skyrim than with Fallout 4, so I personally choose not to do it. This may or may not be a problem, but if there is no mod for Cleaned DLCs, then it is something that should be discussed with the list author.

Now that we've had our brief look at MO2, go ahead and launch xEdit. Load all modules, and wait for the Messages tab to say `Background loader: finished`.
  -  *Most modlists will come with tools preinstalled and preconfigured. If xEdit/SSEEdit/FO4Edit aren't in the list of executables in MO2, add it yourself.*

Right click anywhere in the left pane and select `Apply Script`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6a2997d302c1b78584d07849b94e388866937bc1/images/testing3.png)

Run the `Apply filter for deleted navmeshes` script. Use the filter at the top to help find it if you like.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6a2997d302c1b78584d07849b94e388866937bc1/images/testing4.png)

This may take a minute or two to finish. When it's done, only the plugins with deleted navmeshes will be listed in the left pane.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6a2997d302c1b78584d07849b94e388866937bc1/images/testing5.png)

Deleted navmeshes in the official DLC ESMs are intentional and should be left alone; ergo, I am not concerned with the first two plugins in this list, `DLCRobot.esm` and `DLCNukaWorld.esm`. Ignore these.

The next one is interesting, though. `An Office Fit For a Mayor.esp`. Expanding it will show two navmeshes have been deleted.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6a2997d302c1b78584d07849b94e388866937bc1/images/testing6.png)

This is a HUGE red flag. Anything referencing these navmeshes will instantly crash your game. So you can go ahead and fail this modlist right here and now, right?

Well, not quite. There are some situations in which this is not such a big deal. This mod, for example, combines the three navmeshes in this cell and merges them into one, and nothing is left to reference the two deleted ones. Perhaps not the best or cleanest method, but it does work. However, this still is very much worth noting and discussing with the modlist author, and doing some in-game testing, so let's write down that cell name for later: `DiamondCityEntrance`.

Take note of the next three mods as well, as they all have deleted navmeshes. Remove the filter when you're done, and have a look at those mods again to see if there are any replacement navmeshes in use. It's not uncommon for certain authors to rebuild a navmesh from scratch and use that instead - especially for a mod that completely redesigns an interior cell.

In any case, now you know how to check for deleted navmeshes, which can be extremely problematic for any modlist. Let's move on to another test.

Ensure you don't have any active filters (right click anywhere in the left pane and select Remove Filter). Let's use a new filter!

Right click anywhere in the left pane and select `Apply Filter`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6a2997d302c1b78584d07849b94e388866937bc1/images/testing7.png)

Uncheck everything except the `deleted` flag on the left side.
  -  *The "child" checkboxes don't matter since the "parent" checkboxes are not selected.*  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6a2997d302c1b78584d07849b94e388866937bc1/images/testing8.png)

Now we are shown all the plugins that have deleted references:  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6a2997d302c1b78584d07849b94e388866937bc1/images/testing9.png)

Again, we can ignore the official DLC ESMs. Let's have a look at `Crafting Mastery.esp`. Alt-click the plus (+) sign to expand all.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6a2997d302c1b78584d07849b94e388866937bc1/images/testing10.png)

Just one record here with 0 references and 0 overrides. In other words: who cares! This is not important.

This is basically what you'll do for each deleted reference. If something is referencing them, similarly to deleted navmeshes, it may cause a crash for players. Best practice is to simply use xEdit's QuickAutoClean function on these plugins to "Undelete" these references - which will change the `Deleted` flag to `Initially Disabled` and potentially move the object to -30000 units on the z axis. Now the reference still technically exists, so something referencing it wont be referencing deleted data. Therefor, no crash. Yay. Could you also run QAC on Crafting Mastery above? Yes, absolutely. Will it make a difference? In that specific case, no, because it has no references.

Now that we've covered navmeshes and deleted references, which are by far the **two most important things when testing a list**, we can do some more tertiary things. I personally like to scroll all the way to the bottom of the load order and have a look through any custom patches the modlist developer has made. How are they handling conflicts? Do they seem to understand how to use xEdit and make patches? For example, "[everything is green so it must be good!](https://github.com/LivelyDismay/Learn-To-Mod/blob/58b4e895fd7885a0bd703b3b86685961d479fd2e/lessons/Conflict%20Basics.md)" is a terrible thought process.
  -  *Note: if there are no custom patches, that's a really big red flag. Premade patches are generally designed with two specific mods in mind, not hundreds of mods all loaded together.*

I also like to check all patches for errors. Click the last plugin in the load order, shift-click another plugin a bit higher. All plugins in between the ones you clicked will be selected. I'm just going to select all of my `Crafting-` patches here because...Fallout 4 is kinda janky and will show me tons of Precombined Mesh errors in some other plugins, which is basically all junk data that we don't need to worry about right now.

Right click any of the selected plugins and click `Check for Errors`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6a2997d302c1b78584d07849b94e388866937bc1/images/testing11.png)

Nothing of note was found. Neato.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6a2997d302c1b78584d07849b94e388866937bc1/images/testing12.png)

Does this mean these plugins are perfect and error-free? No! It just means these plugins don't reference anything that's been deleted, which is a great first sign. If anything had popped up with a message like `<Error: Could not be resolved>`, then something else is wrong, such as a broken reference or an improperly removed Master file, as a few quick examples.

Feel free to check for errors in as many or as few plugins as you like. I would also strongly encourage you to simply expand some of the patches and see what exactly is going on in there.
  -  *Do note that this test is **not** about looking for perfection. Every modlist will have some inconsistencies and issues, and that's fine. The point of this process is to make sure that the modlist developer shows signs that they know what they're doing, are capable of patching, show a willingness to improve, and that the list is getting proper attention.*

It's really easy to get hung up on little things, but let's be honest here: nobody sees everything. I spent months working on Magnum Opus, and I still find issues all the time. The important thing is that the issues are not game-breaking and I know how to fix them. When I first submitted it for testing, one of the official Wabbajack testers found a hundred issues I hadn't noticed...and he found them in about five minutes. I'd just been so focused on other things that I totally glazed over some of the basics. *It happens, and it's okay.*

Now we do in-game testing. We wrote down a cell name earlier, if you recall: `DiamondCityEntrance`. Let's start there. Just coc from the main menu.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6a2997d302c1b78584d07849b94e388866937bc1/images/testing13.png)

Now we're in Diamond City.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6a2997d302c1b78584d07849b94e388866937bc1/images/testing14.png)

Run around a bit. Monitor the NPCs. Moving isn't crashing, NPCs are getting around normally, everything seems fine. If the navmeshes here were truly broken, the game most likely would have crashed the moment it tried to even load this cell. If you want to test it even further, grab yourself a follower and see if they can properly navigate the environment. 

Another good test for in-game performance would be what I call a "stress test" on the engine. Go to any outdoor cell and use the following console commands:
  -  `tgm`
  -  `tcl`
  -  `player.setav speedmult 800`

Now run! You'll be moving like Sonic the Hedgehog and never running out of stamina or taking any damage. This is forcing the engine to load *entirely too much crap at once*, which it is 100% not designed for. Feel free to spawn in a few dozen NPCs or dragons or whatever while you're at it, see how much it can take...plus it can just be kinda fun to watch 20 giants fight 40 dragons after spending three hours poring over records in xEdit, you know? Have a little fun with it.

As I said earlier in regards to creating a modlist, it's nigh impossible to find everything. This is why we require multiple testers to approve a list before we accept it for "official" status on Wabbajack. All we ask is that you do your best, report your findings, and most importantly, **ask questions**. Nobody knows everything. We all have different areas of expertise and interests, so we can combine to form a modding Voltron to address whatever issues arise.

Just do your best. We're all here to help. Thank you for reading, and good luck!
