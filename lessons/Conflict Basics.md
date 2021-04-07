# Conflicts: Learning How To Read xEdit

The word “conflict” inherently evokes thoughts of fighting and negativity. When someone tells you that “you gotta fix the conflicts in your modlist” then you immediately think “oh no, I need to make my mods stop fighting and fix them!” Right?

WRONG! NO! I NEED CONFLICTS. Conflicts give me life. They give me purpose. They give you purpose, too. If they didn’t, you wouldn’t be reading this. What I think we need is a new perspective.

Conflicts aren’t bad. They are **necessary**. In modding, “conflict” is synonymous with “something changed.” Mods are designed specifically to change the game in some way. With this worldview, it is obvious to see why conflicts are not bad, but are required.

Let’s have a look at some different types of conflicts. Launch xEdit.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/ConflictBasics1.png)  

Load all modules.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/ConflictBasics2.png)  

Wait until the right pane says `Background loader: finished`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/ConflictBasics3.png)  

Click any plugin in the left pane. The right pane’s view will swap to that, but that’s not exactly what we’re concerned about here. Look in the top right corner. There is a button labeled `Legend`. Click it.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/ConflictBasics4.png)  

You’ll get this fancy pop-up. Since it is its own window, you can move it wherever.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/ConflictBasics5.png)  

Keep it a bit out of the way, but in a place that’s easy to reference when needed. For example, I used to keep it down here:  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/ConflictBasics6.png)  

Note: your color scheme may be a bit different from mine because I think Light Mode is the devil’s work. If you want to change yours, open the Options Menu:  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/ConflictBasics7.png)  

And customize the UI Theme tab to your liking:  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/ConflictBasics8.png)  

Anyway, back to conflicts. The Legend pop-up explains them all quite simply. I’m more of a hands-on learner though, so let’s have a look at examples of each. I’m assuming you still have whatever random plugin you clicked earlier highlighted and displayed in the right pane, so that will be your first lesson. Easy! Single Record - plain background with white text. No overrides, no conflicts, no problems. The information exists as-is. Nothing to worry about.

Let’s find another. Head to `StandaloneWorkbenches.esp` and expand the `Furniture` category. You’ll see one single conflict here for `FE000821 wSW_ManufacturingWorkbench`. Click it!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/ConflictBasics9.png)  

You’ll see just one little conflict: I renamed this workbench, and the name on the right is bright green on a yellow-green background. Looking at our Legend, that tells us that this is an `Override without conflict`. In other words, The base record was changed once, and nothing else is overwriting that single change. In essence, *this isn’t really a conflict*, because nothing is fighting for control here. What do I mean by “fighting for control”? Let’s find an example of that!

Find `Crafting Mastery.esp` in the left pane and expand it, then expand the `Constructible Object` category.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/ConflictBasics10.png)  

So many colors! But you’ll notice - probably right away, I hope - that they’re all bright green text on a yellow-green background. Without even opening each of these records, we already know what that means: Override without conflict. Something in this mod is overwriting a setting from a base plugin, and nothing is fighting it. Skip all of these! Scroll down until you see RED.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/ConflictBasics11.png)  

Well that looks scary. Let’s have a look at `06025B1A  co_weap_throw_DLC04PackScentGrenade`. Scroll through the right side until you see that scary red again.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/ConflictBasics12.png)  

Now HERE is a conflict worth looking at. `DLCNukaWorld.esm` says one thing, `Crafting Mastery.esp` says another thing, then `Crafting-VanillaItemKeywords.esp` says another thing, and none of them agree with each other. Let’s take a closer look at each of them.

DLCNukaWorld.esm wants Predator Grenades to be craftable at the Chemlab under the GRENADES filter after the Player has completed Quest Stage 50 of DLC04MQ04.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/ConflictBasics13.png)  

Crafting Mastery.esp wants Predator Grenades to be craftable at the Explosives workbench under the GRENADES - SPECIAL category after the Player has completed the quest “An Ambitious Plan” AND Quest Stage 500 of “Home Sweet Home” AND Quest Stage 50 of DLC04MQ04.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/ConflictBasics14.png)  

Crafting-VanillaItemKeywords.esp wants Predator Grenades to be craftable at the Explosives workbench under the GRENADES - SPECIAL category after the Player has completed Quest Stage 500 of “Home Sweet Home” AND Quest Stage 50 of DLC04MQ04.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/ConflictBasics15.png)  

THIS is a conflict. Multiple records doing different things to the same record and not agreeing on the changes being made. Now, will anything here break if this Conflict isn’t fixed? **NO**. This is *exactly* how I want it. Referring back to the Legend we have open, the red text on a red background means `Conflict loser`. This means it WAS an override, until another plugin got loaded after it and said “no, I don’t think so” and told it to go away.

If I forward that Conflict loser so that it does get loaded, does that break anything? Again, **NO**. I know, it’s all nice and green now, but the color is only telling you what type of conflict you’re looking at.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/ConflictBasics16.png)  

**This is the most important thing I can possibly teach you about xEdit: RED DOES NOT MEAN BAD, AND GREEN DOES NOT MEAN GOOD**. Get that thought out of your head right now. The colors are only showing you what TYPE of conflict you’re looking at. The colors are NOT showing you good versus bad.

To look at this yet another way, let’s change our perspective just a little bit one more time. Right now we are in the Crafting Mastery.esp plugin’s contents, and `co_weap_throw_DLC04PackScentGrenade` is that scary red color.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/ConflictBasics17.png)  

Right click `Crafting-VanillaItemKeywords.esp` at the top of the right pane here and select `Jump to`. We’re still in the same record on the right, but look at the left pane.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/ConflictBasics18.png)  

This is what I mean by perspective. `Crafting Mastery.esp` was losing its fight, so it was in red. `Crafting-VanillaItemKeywords.esp` is winning, so it’s displayed differently - in this case, `Identical to master but conflict winner`, because all of its information exist in the exact same state as the plugin before it - `Crafting Mastery.esp` - with one single exception. And that exception is the condition added by Crafting Mastery that is no longer present in this plugin. Thus, Identical to master but conflict winner.

I know this may seem incredibly basic to some of you...and after doing this for a while, it does seem basic. But I remember very clearly when I first started using xEdit. I had no idea what I was doing. I didn’t know that Legend existed. I had no resources I knew of to get help. It sucked. I don’t want you to go through that. It is so, so important to understand what these colors mean.

Leave the Legend open while you’re working until you never need it again. It will become second nature before long, don’t worry.

Close xEdit when you’re ready. And since I was fiddling about with making things green, I’ll get a prompt to save. Uncheck this box - I don’t particularly want to save the change I made.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/ConflictBasics19.png)  

But will it break the game if you do save it?

I think you know the answer.
