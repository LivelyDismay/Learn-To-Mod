# OMODs: What They Are and How They Work

If you went through my earlier lesson about adding and patching weapon mods, you may recall a brief mention of OMODS - Object Modification records. These are things you add to existing weapons and armors: scopes, receivers, armor lining, things of that nature. Anything that enhances/changes something you have in your inventory. Thus the name *Object Modification*.

So how do they work, and why didn’t we need to patch them for workbench keywords? Let’s find out!

Note that this lesson will also expand on more Keyword functionality as well, so if you’re interested in that, this may be worth reading.

Let’s jump right in. Launch xEdit.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/f0066fe771a2f79547bdac20bd577f7cc281773b/images/Omods1.png)  

Load all modules.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/f0066fe771a2f79547bdac20bd577f7cc281773b/images/Omods2.png)  

Wait until the right pane says `Background loader: finished`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/f0066fe771a2f79547bdac20bd577f7cc281773b/images/Omods3.png)  

In the FormID search bar in the top left, type in `148338` and press Enter.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/f0066fe771a2f79547bdac20bd577f7cc281773b/images/Omods4.png)  

You’ll be jumped down to the `mod_10mm_Receiver_MoreDamage1` record. This is an OMOD for the 10mm pistol. Specifically a Receiver attachment. And it makes the gun do more damage. Who would’ve guessed? Let’s take a look at how this works on a more technical level.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/f0066fe771a2f79547bdac20bd577f7cc281773b/images/Omods5.png)  

In the right pane, you’ll see a pretty large collection of Keywords here.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/f0066fe771a2f79547bdac20bd577f7cc281773b/images/Omods6.png)  

These are called Attach Points. Take note of the first one at the top: `ap_gun_receiver`. This is telling the engine that this specific OMOD can be attached to a weapon with this Keyword, because that’s the slot on the weapon it gets attached to. Makes sense, right? So let’s see that in action a bit.

First, click the `mod_10mm_Receiver_MoreDamage1` record in the left pane. Now press `Control+1`. The left pane will swap to the Messages tab even though there’s nothing new there. What we just did was “Bookmark” this record. We will come back to this.

For now, type `4822` in the FormID search bar in the top left and press Enter.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/f0066fe771a2f79547bdac20bd577f7cc281773b/images/Omods7.png)  

You’ll be moved to the record for the 10mm pistol. Press `Control+2`. Again, swapped you over to the Messages tab, because we bookmarked it.

Now press `Alt+1`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/f0066fe771a2f79547bdac20bd577f7cc281773b/images/Omods8.png)  


Welcome back to the original OMOD record we were looking at!  
Now press `Alt+2`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/f0066fe771a2f79547bdac20bd577f7cc281773b/images/Omods9.png)  

Welcome back to the 10mm weapon record! Bookmarks are great.

Scroll down a bit in the right pane and look at the `APPR - Attach Parent Slots` Keywords section. See how it has a keyword for `ap_gun_receiver`? That means this weapon can have OMODs attached to the receiver slot - for example, the one we were looking at earlier. Nice!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/f0066fe771a2f79547bdac20bd577f7cc281773b/images/Omods10.png)  

Press `Alt+1` again to head back to the OMOD record. So now we know what that Attach Point keyword is for. What about the Attach Parent Slots directly below it?
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/f0066fe771a2f79547bdac20bd577f7cc281773b/images/Omods11.png)  

Well, they’re fairly self-explanatory, but let’s cover it anyway. The first one - `ap_gun_Dot` - lets you choose which sights you’re attaching. You know, Dot Sights, Iron Sights, Reflex Sights, etc. `ap_gun_ProjectileNode` and `ap_gun_Barrel` are both for barrels, such as Long Barrels, Ported Barrels, and things of that nature. Mag is for Magazine (Extended Mag, Quick Reload Mag), Scope is for...scopes….(ACOG Scope, 4x Zoom Scope), and Casing is for Receivers (Powerful Receiver, Hardened Receiver). These are all the sub-menus in the Weapons Workbench when you are modifying the 10mm Pistol.

Below the Attach Point keywords, we have sections for `Property`. The data is named a bit strangely, but you get used to it. Let’s check out the first one.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/f0066fe771a2f79547bdac20bd577f7cc281773b/images/Omods12.png)  

Let's go through this information line by line.

A float is a variable. Or, in other words, a number. Yep, that’s it. Simple.  
**MUL**+**ADD** is the Function Type here, which means it will **Mul**tiply and then **Add** the float variable to the base weapon’s variable.  
The Property (AttackDamage, in this case) is saying WHICH variable from the base weapon is being modified by this Float value.  
The float value here is below the Property: `0.250000`.  

So put this all together, and what does it mean? Well, you can press `Alt+2` and check the base damage on the 10mm pistol, but I can tell you right now that it is 18.

Anyway, back to that Property. What does it mean? It means exactly this: It’s going to take the 10mm’s base damage of 18, multiply it by 0.25, then add that result to the original base damage of 18. 18 times 0.25 is 4.5, 4.5 plus 18 is 22.5, so having this specific attachment applied will increase the 10mm’s base damage from 18 to 22.5. Quite a nice improvement for sure.

The next two Property sections are extremely similar, and I’m willing to bet you can now easily decipher what they are. Take note of the Property they’re modifying with the Float values: Value and Weight, specifically. So not only does this attachment increase the gun’s damage output, it also increases how many caps it’s worth and how heavy it is in your inventory.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/f0066fe771a2f79547bdac20bd577f7cc281773b/images/Omods13.png)  

This fourth one is a little strange though. It seems to be adding a Keyword to the weapon when this receiver is attached, right?  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/f0066fe771a2f79547bdac20bd577f7cc281773b/images/Omods14.png)  

Why yes, yes it is. Why would it be doing that? Well, you know how those names for your weapons get all crazy and long in the game? “Hardened Powerful Automatic Night Vision Combat Rifle” for example? Well, all those additions to the name are handled by keywords, which are then referenced by INNRs - Instance Naming Rules. Keywords handle everything in this engine, I swear.  

So this one adds the keyword `dn_HasReceiver_MoreDamage1` to the 10mm Pistol after you attach it. You could track this down in the INNR records to see what it does for yourself, but that takes a while and who really has time for that anyway.

Well, I do, so you’re in luck. This shows that if a weapon has the keyword `dn_hasReceiver_MoreDamage1` attached, then it will add the word Hardened to the name. Hardened 10mm Pistol.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/f0066fe771a2f79547bdac20bd577f7cc281773b/images/Omods15.png)  

Take that same Pistol and add an Armor Piercing Rounds attachment, and you get this: Hardened Piercing 10mm Pistol. Makes sense, right?  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/f0066fe771a2f79547bdac20bd577f7cc281773b/images/Omods16.png)  

Hopefully you can now read this type of record in xEdit to figure out what exactly they’re doing, how they are applied, and *how Keywords continue to be the masters of the universe*.
