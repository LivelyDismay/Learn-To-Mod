# Conditions: How to Make Your Game a Unique Experience

Conditions are great. They offer a wonderfully diverse array of ways to offer content, and really allow you to be creative with how you present your work. And they are, much like Keywords, used for everything. Load screens, perks, crafting...all handled by conditons.

So let's have a look at some! Today we will just be dealing with vanilla Fallout 4 + the official DLCs. Easier to follow along with me that way.

Launch xEdit.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions1.png)

Load all modules.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions2.png)

Wait until it says `Background Loader: finished`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions3.png)

Let's start with a simple one. Expand the `Fallout4.esm` plugin, then head down to the `Load Screen` category. Expand that as well. Select the second record: `Vault111CharGen`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions4.png)

Shockingly, we are focusing on the Condition here. Expand that to get a better look at what's going on.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions5.png)

Pretty simple, really.  
`Type: Equal to` - dictates how to use the information directly below this line.
`Comparison value 1.00000` - 1 = true. 0 = false. As the line states above, the condition for this must equal 1 (true) to have any effect. What conditons must be true, exactly? Let's keep going.  
`Function: GetInCell` - checks which cell you're in. So someone or something has to be in a specific cell for this to be true. Which cell?  
`Cell: PrewarVault111` - this cell!  
`None` - ignore this, it is useless junk data.  
`Run On: Subject` - "subject" is whatever is being targeted by this specific condition. In this case, it is you, the player.  
The other two lines below this are also junk data. The `Parameter` will always be `-1`. Changing this will break it. Don't change it.  

So put that all together, and what do we get? Easy: the Subject must be in the PrewarVault111 cell in order for this to be true. And as long as this is true, this loading screen will show up in your game.

Seriously. That's it. That's all there is to this one. And since you're only ever in this cell one time for the entirety of the game, this load screen can only be seen once. Since the Subject is never, ever in this cell again, this Condition will always be false (or, to put it another way, it will never equal 1 or be true), and the loading screen will never be seen again.

Neat! Let's look at something else. Type `46946` in the FormID search bar in the top left and press Enter. You'll be jumped down to this record:  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions6.png)

This is a COBJ record, or Constructible Object. Again, pretty easy to read: if you have two `Bloatfly Meat`, then you can create the `Baked Bloatfly` object at the Cooking Workbench under the `ROAST` category. But this doesn't have any Conditions, so what the hell are we doing here?

Well, we're going to add some! For practice, you see.

Right click the top of the record in the right pane and select `Copy as override into...`  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions7.png)

Choose the `<new file>` option with the ESL flag in the right column. This is the kind of plugin you'll want to make 99% of the time.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions8.png)

Name it whatever you want.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions9.png)

Now we have an exact duplicate of this record in our own custom plugin. This is where we can make our edits - or patches, if you will.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions10.png)

Right click in the blank `Conditions` section in our new record, and select `Add`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions11.png)

Now we have this new green block. Yay, progress!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions12.png)

Expand it to get a better look.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions13.png)

For this exercise, we will add a Perk requirement to this. This single sentence gives us a ton of information to get started with. We want the Player to have a specific Perk.

Ergo, we need, at the bare minimum, for this to be True ("the player has this thing, yes"). So change the Comparison Value to 1.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions14.png)

Now the player can't have more than 1 of any single specific perk (as each Rank of a perk counts as a totally new perk) so leave it set to `Equal to`. We do, however, know we want this to run on the Player. There are two ways to do this:

1. Leave it set to Subject. Since the Condition is checking against whomever is using the crafting station, it's already going to be checking the player, because the player is the subject.  
2. Change the `Run On` to `Reference` and select `PlayerRef` in the box that pops up below it.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions15.png)

In this case, again, Subject and PlayerRef do the exact same thing, since the Player is the Subject. But it's still important to know the distinction.

Next up: `GetWantBlocking` isn't what we want. We want a Perk, right? So let's change that.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions16.png)

A new box has popped up. Choose a perk! The dropdown will show you all the perks you can choose from.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions17.png)

And just to show you how much variety there is here, I'll choose something outrageous for fun - just as an example that shows that there are a lot of Perks besides just the ones in the level up menu.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions18.png)

Now you have to be Well Rested to craft this thing. Why not? It's my game, I can do whatever I want. So can you!

Let's add another.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions19.png)

For this Condition, I've made it a requirement that the Subject has 1 Cooking Pan in their inventory.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions20.png)

Unfortunately, this is broken! It may not seem obvious, but you have to pay *extremely* close attention to Conditions. Look at the top two lines: Equal to 1. This says the Subject has 1 Cooking Pan. Not 0, not 2, not 14. Just 1. So if the player has 2 Cooking Pans in their inventory, this Condition is now false, and the item can't be crafted. So let's change that a bit. Double click where it says Equal To, and you'll get this handy dropdown menu:  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions21.png)

Select the `Greater` checkbox.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions22.png)

And now it says `Greater than or equal to`. Perfect! Now they NEED 1 cooking pan...or more!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions23.png)

You may also have noticed a checkbox there that says `Or`. All Conditions are `AND` Conditions by default - meaning every single condition must be true in order for...whatever it's editing to show up in the game. So let's try out an `OR` condition.

Add another!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions24.png)

Drag and drop the Cooking Pan condition into this one. It'll just save us a little bit of time. Remember: You have to drag from the top (parent) slot in the Condition entry into the parent slot of the new Condition.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions25.png)

Now we've got duplicate Conditions!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions26.png)

Let's change that Cooking Pan line to a Cooking Pot line instead.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions27.png)

Now add the `Or` condition Type to both the Cooking Pan and Cooking Pot requirements.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions28.png)

Minimize all the Conditions so you can read them all on a single line next to each other.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions29.png)

See how the first one ends with `AND` and the other two end with `OR`? This means exactly what you think: The player needs the Well Rested perk, AND at least one Cooking Pan OR at least one Cooking Pot.  

Now let's say I want to add these exact conditions to all the food in the game. It's pretty time-consuming doing these one by one, right? Right! It sucks! So let's do them all at once in about ten seconds!

Select all the other records you'd want these Conditions applied to, then right click and `Copy as override into...`  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions30.png)

Select the patch we just made a few minutes ago.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions31.png)

Click any of the records we have copied - it doesn't matter which one. Then right click the top of the new plugin's name in the right pane and select `Jump to`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions32.png)

Our right pane hasn't changed, but the left pane has. Now we're looking at this record from the perspective of our patch.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions33.png)

Select all of these records in the left pane, right click, and select `Compare Selected`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions34.png)

Now we have a whole mess of records in the right pane. Scroll all the way to the bottom, to where the Conditions are.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions35.png)

Right click the Conditions header there, and select `Copy to selected records`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions36.png)

We want the conditions applied to all of these records, so click OK.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions37.png)

And just like that, all of these COBJ records have the same Conditions. So fast! So efficient!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/85dbbac06b49ece34da86376fef58d5a82d80114/images/conditions38.png)

There are TONS of options for Conditions. Some of my favorites are `GetQuestCompleted`, `GetLevel`, `GetIsSex` (for making gender-specific conditions), `GetIsRace`, and `GetLocationCleared`, just as a few examples of the sheer quantity of different things you can try. And you should try a ton of them! Absolute freedom lies within.

