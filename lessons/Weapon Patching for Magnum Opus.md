# How to Properly Add and Patch Weapon Mods for Magnum Opus

---

Check out my [One Minute Modding](https://youtube.com/shorts/Qd_1V5y68AY?feature=share) video on workbench patching, or read on if you prefer text format.

---

So, Magnum Opus is pretty much what you wanted about Fallout 4, but god dammit, you just really want this one gun mod you particularly enjoy...but you just don't know how to add it to the list properly. Lucky for you, I enjoy teaching! Let's add a mod together.

For the purposes of this exercise, I'll add the [FACTOR Modular Rifle](https://www.nexusmods.com/fallout4/mods/32908). We will be using the FULL version. Go ahead and download that, then install it in MO2 and activate it. If prompted, do not unpack the ba2 archive. 

So we've got Factor installed and active. The plugin is right there at the bottom of the load order - if it isn't, make sure it's sorted by Priority! Now we launch xEdit.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch1.png)  

Load all modules on the pop-up here.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch2.png)  

Then wait! Don't touch anything until the right pane says `Background loader: finished`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch3.png)  

The first thing I'll do is start the Crafting patch. Expand the Constructible Object field (often referred to as COBJs). Most authors follow the same naming convention: a prefix for their mod as a unique identifier, followed by the standard vanilla naming scheme. `co_mod` is an OMOD, or Object Modification. These are applied at a Weapons Bench, and thus do not have a BNAM, or Bench Name. The BNAM field is what dictates where an object is crafted. You can see here that this `co_mod` record has no BNAM. This means we have nothing to do here (for now, at least).  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch4.png)  

A bit lower, however, we see `co_Bolt`. Sounds like ammunition to me. Let's have a look.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch5.png)  

Here we see a standard cobj. The Components are what the player needs in order to craft it - in this case, 1 Steel. Below that is the Description displayed in the Workbench when selected, the Created Object, the BNAM, the Category, and the Created Object Count. These are all important...and very self-explanatory. 1 Steel creates 4 bolts when crafted at the Chemlab, and it is found under the category entitled `"Factor" - Weapon and Ammo`.

Surprisingly, however, the bolts aren't actually ammunition - it's actually a weapon. Let's jump to that record to see what exactly it is. To do so quickly, Control+Click on the Created Object field in that Cobj.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch6.png)  

Weapon records have a lot of...irrelevant data. The important parts are pretty self-explanatory, as much of xEdit's records are if you just sit here and read them. The EquipmentType is occupying the GrenadeSlot, so it is a thrown weapon. It does no damage, does not dismember enemies, is silent when thrown, and has ImpactData equivalent to the player's footsteps. This is what is distracting enemies when this weapon is thrown - you're essentially "throwing" a footstep for enemies to investigate.

Now that we know what a Bolt is, let's head back to that cobj. Right click that record in the left pane, and `Copy As Override Into...`  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch7.png)  

Since FACTOR is the last plugin in our load order, we can't copy it as override into any existing plugin - because FACTOR is already loaded AFTER everything else. Plugins loaded before it obviously can't override something loaded after it, so we have no choice but to create a new plugin. Which is fine, because that's what I want to do anyway.

You will see this window with some options for what type of plugin you wish to create. 99% of the time, you want the one selected in the image here. It is an .esp file with an ESL flag, as seen on the right side. This means you can manipulate the file freely in your load order, but it doesn't occupy one of your main 255 plugin slots. In essence, it gets "merged" with all your ESL-flagged plugins when the game is launched.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch8.png)  

Name it whatever you want. I tend to name everything `Crafting-` then the name of the mod I'm patching. Easier for me to find.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch9.png)  

Now we have a clone of that cobj in our own plugin. As it is right now, this is known as an `ITM - Identical To Master`. That means nothing is changing...which kind of defeats the whole purpose of modding and patching, when you think about it logically. If you're ever unsure what the colors do, note the Legend button in the top-right corner. Click it. Leave it open for as long as you're working, until you never need it again. Read more about xEdit basics [here](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/lessons/Conflict%20Basics.md)!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch10.png)  

Now here is where xEdit can be a bit...weird. We need to add masters to this patch, so let's do that real quick.

A quick way to get to your new patch is to right click it at the top and select `Jump To`.
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch11.png)  

Right click your new patch and select Add Masters.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch12.png)  

Magnum Opus 100% relies on Lively's Keywords Resource and Standalone Workbenches for crafting. **These are not optional**. Add these masters to your patch.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch13.png)  

Now to ensure xEdit allows us to actually use those masters, close and save. Make sure the new patch is selected here.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch14.png)  

Your new patch is at the bottom of your load order. Activate it.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch15.png)  

Launch xEdit again, selecting all modules like you did earlier. Once the background loader is finished, scroll all the way down to your patch and open up your cobj record.

Double click the BNAM field in your patch.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch16.png)  

Type in wsw and it will begin to autofill. All of the Standalone Workbenches are prefixed with `wsw`. Scroll down to the Weaponsmith Workbench.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch17.png)  

Now we want to change the Category, to be more in line with how Opus categorizes everything. Double click that, and type in `lkr`. Just like before, it will begin to autofill.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch18.png)  

There are a LOT more keywords than workbenches, so you can type a bit more if you want.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch19.png)  

For this, I'd likely go with Unconventional Weapons.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch20.png)  

Now we have a new BNAM and Category keyword.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch21.png)  

And we all know I'm a bit of a grammar nazi, so I added a comma. Don't judge me.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch22.png)  

Once you do this as much as I do, you tend to learn which cobj records have a BNAM and which don't, just based on a quick glance. So I'll control-click all the ones I know have a BNAM and copy as override into my new patch all at once.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch23.png)  

In this case, it's just the gun itself and two forms of ammo. Unlike before, however, we have a new option.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch24.png)  

We don't need to make a new patch, obviously. We just made this one! So let's copy it into our existing patch. Now we have new cobjs in our patch.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch25.png)  

Since this patch already has the masters we need, we can just move on and repeat the process that we did for the bolt, selecting appropriate workbenches and keywords as we see fit.

Doing this one by one can be a hassle, especially if I have dozens of records that I'm moving to the same workbench. So, with the two Ammo cobjs we have, let's do what would be a faster way if there were a lot more. (This isn't terribly useful for just two records, but it will be extremely useful in a lot of other scenarios, so might as well learn it.)

You can see here I've moved this to the Ammunition crafting workbench. I have NOT touched the RailGun ammo cobj yet (which is why it is green instead of yellow).  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch26.png)  

Control-click those two ammo records and select Compare Selected.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch27.png)  

Now you have both of those records on the right side for comparison.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch28.png)  

You can see the BNAMs don't match, which is what we're here to fix.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch29.png)  

One option is to simply drag and drop from one record to the other - and this is what I would normally do with just two records as seen here. But like I said, I'll teach you another way for future reference.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch30.png)  

Right click the Ammunition bench BNAM from the first plugin, and select Copy to Selected Records.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch31.png)  

We only have two records selected, and we're copying FROM one, so we only have one option here. But again, if we were doing this to dozens of records at once, this is MUCH faster than the drag-and-drop method, or manually editing each one.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch32.png)  

And now they're both set to the Ammunition workbench. Excellent.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch33.png)  

For the RailGun ammo category, I've already made a keyword specifically for this one entry. Fancy!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch34.png)  

Now let's go back to that weapon cobj. See how the Conditions are blank? Right above the Created Object?  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch35.png)  

This is bad practice. It means the player can craft this weapon as soon as they start the game. That's not terribly balanced. So, let's add some conditions! This is where you can get REALLY creative.

Right click and select Add. Remember - we're editing the patch here, not the Factor mod itself.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch36.png)  

It always defaults to this on a new addition. Click the little + next to Condition to expand it.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch37.png)  

Now we can have some fun.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch38.png)  

Let's start simple and add a requirement of Level 20. Just edit the values as seen here.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch39.png)  

Again, self-explanatory. PlayerRef (that's you!) must be equal to or greater than Level 20 to craft this.

So why PlayerRef and not Subject? Honestly, in this case, *it's the same thing*. I just use PlayerRef out of habit. But to expand on that:

PlayerRef is the player, 100% of the time, no matter what.

Subject is whatever this action is being targeted on. Since this Condition is for crafting this weapon, and this action is checking if the Subject using the workbench is level 20, and...the Subject using the workbench IS the Player...Subject and PlayerRef are identical in this case.

But that's neat. Conditions are easy! Let's make another.

Add another.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch40.png)  

Expand it.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch41.png)  

Now the player needs Gun Nut rank 3. Also notice how the condition above for the level 20 requirement ends with AND - this means the player needs to fulfill ALL conditions to craft this weapon.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch42.png)  

Add as many conditions as you want. Or as few as you want. It does not matter. The only real stipulation is that the game can only show the player a maximum of TWO perk requirements on the crafting screen. FallUI - Workbench increases this to 8, thankfully, but vanilla can only show 2. So if you add 3 perk requirements, the player does in fact need them all...but the game only shows you two, and players can get confused about why they can't craft something when the game is apparently telling them they can. The third perk requirement is effectively hidden by the crappy UI limitation. *This is not an issue in Magnum Opus, I'm just telling you anyway, in case you ever wish to release a mod*.  

Also this bothered me so I changed it.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch43.png)  

Normally, now is when I would scroll through the [OMOD records (Object Modifications)](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/lessons/OMODs%20Tutorial.md) looking for typos, grammatical issues, and off-balance things. I'll skip that for now. Let's move on to running our fancy Item Sorting script.

But first, we need to move our Crafting patch in the load order a little bit. Close xEdit and save your new patch.

I keep all of my Crafting patches inside the `Methodology` folder. You may wish to simply make your own custom folder in case you ever update with WJ. The Crafting patches in the load order are also alphabetized. It's easier for me to find them that way, and they obviously don't interact with one another, so this doesn't cause any issues. But the crafting patch DOES need to be below the Factor mod itself, so let's just move both of those to right below Lively's Tweaks for now. We can always adjust this later. The important thing is that these plugins are ABOVE R88_SimpleSorter.esp.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch44.png)  

Go ahead and launch xEdit one more time, selecting all modules to load. When background loader is finished, right click anywhere in the left pane. Seriously, anywhere. Doesn't matter what you click on.

Select Apply Script.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch45.png)  

We are running M8r Complex Sorter. Use the filter to find it, or scroll through the list.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch46.png)  

Fancy! This script has a ton of built-in functionality. Fortunately...we don't really need to touch anything! It's literal fucking magic. You can make a new esp if you want to be safe, or make a backup of the one that already exists. It doesn't much matter. This script can be ran as many times as you like.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch47.png)  

So just click Generate Patch when you're ready.

NOTE: If you get an error about a specific file path cannot be found, follow the file path in the warning and create a new folder called `cache` where the program is expecting it to be found.

This will take a while! Be patient, just let it work.

xEdit will tell you when it's done.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch48.png)  

You can even see here that it added a `[Grenade]` tag to the bolts. This is because the sorter is based on Keywords. The Bolt has a WeaponTypeGrenade keyword, so Complex Sorter calls it a Grenade. If you wish to change this, you can manually edit it, create an override patch, or edit the script directly so that it automatically sorts it how you like it in the future. But that's a lesson for another day, so let's just move on.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch49.png)  

Close xEdit and save your sorting plugin.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch50.png)  

Also worthy of note: most weapons WILL NOT have obvious tags like this `[Grenade]` tag here. This is a bit more complicated. Weapons are named via INNR records - Instance Naming Rules. These are a bit more complicated, and again, we won't quite be getting into that today.  

So now let's launch the game and see if our Factor items are properly tagged in-game. Select F4SE from the dropdown in MO2 and launch the game. And make sure your sorting patch is activated in the load order!

This is my default testing cell for things like this. It's a small cell and loads very quickly.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch51.png)  

Since Magnum Opus has ESP Explorer, just press F11 once the game is loaded.

Fancy! It opens all your mods like an inventory menu. Find Factor in this list.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch52.png)  

*Hint: it should be at the very top.*
Everything seems to be tagged appropriately! Excellent!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch53.png)  

I don't know what that is, but it's something I'd have to look at later.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/8834382db6b00fbdb57d2842e24b09e9bd66d093/images/weaponpatch54.png)  

But I think I'll call this lesson complete for today. I hope you learned how to appropriately patch and tag new weapons for Magnum Opus.  
