# Keywords - What They Are and Why You Should Care

Keywords are important. There are so many keywords and uses for them, though, that it’s really, really hard for me to think up a succinct explanation for what they are and what they do. So, let’s try to keep this as simple as possible by looking at a few example Keywords, how they’re used, and what exactly they’re doing for your game. Later on, we’ll even make a Keyword of our own, so you can see how insanely simple it is to make, and just how powerful a Keyword can be when applied in the correct manner.

Like I said, we’ll keep it simple (or as simple as I can muster, anyway). Launch xEdit.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords1.png)  

Load all modules.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords2.png)  

Wait until it says `Background loader: finished` on the right side.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords3.png)  

In the top left corner, you’ll see a search bar marked FormID. Click inside and enter the value `13795`. Press enter.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords4.png)  

You’ll be jumped to this record here: a Keyword named `ActorTypeCreature`. And there is….wow, just absolutely zero information here! Weird, right? Almost looks useless. Until you look just below the right window, specifically at the `Referenced By` tab. 252! Holy shit, why are so many records using this seemingly pointless information as a reference? Let’s take a gander!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords5.png)  

Wow. Okay. That’s a lot of stuff. Let’s make this slightly easier to sort through. In the right window, click the Signature heading at the top. This will just reorganize the entries in the Referenced By tab here, which will in turn make it easier for me to show you how this keyword can be applied in multiple ways, for various results in your game.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords6.png)  

The first one has a signature of FLST, which is short for Form List. This does not really concern us right now, so let’s go with the one below it: an INFO record. Double click that sucker!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords7.png)  

Random line of dialogue. Okay. How does the ActorTypeCreature keyword factor into this? Well, let’s scroll down a bit to the Conditions.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords8.png)  

There’s our keyword. So, what exactly is it doing in this Dialogue record? Well, that’s simple: the NPCs that can say this line of dialogue in combat IF they are fighting something that DOES NOT have the ActorTypeCreature applied to it. And how does the game know a creature is nearby instead of a human or a supermutant? Easy: it has the ActorTypeCreature keyword assigned to it. Why don’t we take a look at an example of that, then? So we can see what the hell I’m talking about here.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords9.png)  

Head on back to that Referenced By tab again and sort by Signature. Scroll down to the first one with the `NPC_` Signature. Also a minor side note here: you’ll notice all Signatures for all records are exactly four characters. No more, no less. Thus the underscore for `NPC_`. This can be important for filtering for things or using the console in-game, but we can cover that another day. For now, let’s have a look at this here Stunted Yao Guai.
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords10.png)  

Scroll down a bit beyond its SPECIAL stats and actor properties. You’re free to read these if you like, they’re straight-forward and just tell you the stats of this particular NPC. But below all that, you can see this here Keywords section:  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords11.png)  

And there it is again: ActorTypeCreature...as well as a few others. Thinking back on that Dialogue line we looked at earlier, we said that line can’t be spoken if another nearby NPC has the Keyword for ActorTypeCreature, so this particular Yao Guai couldn’t trigger that line of dialogue from other NPCs. Neat! I also see an ActorTypeAnimal keyword there, so let’s look at something sliiiightly more complex. Stay with me here, we’re in for a wild ride.  

Head back up to that FormID search bar in the top right and type in `1E67F`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords12.png)  

You’ll be shot down to the Animal Friend rank 1 perk. I know this one looks a little scarier, but bear with me for a bit. Scroll down beyond all the Script Fragments and Entry Points until you reach the Perk Conditions section. You will learn a TON of fun stuff just from this section alone. Let’s take a really close look at it.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords13.png)  

That’s a lot of fucking Conditions, right? You might even notice they all end with `AND` - if you read previous lessons, you may recall this means that the Subject (in this case, whatever NPC is being targeted by the Player) must fulfill EVERY SINGLE ONE of these Conditions in order for the Animal Friend perk to trigger properly. Reading them closely, you should come to this conclusion:
  -  The NPC in question must NOT be a higher level than the player.  
  -  The NPC in question must NOT have the ImmuneToHoldupKeyword.  
  -  The NPC in question must NOT have a HoldupImmune value greater than 0.  
  -  The NPC in question is NOT a Companion.  
  -  The Player must be aiming at the NPC in question with a weapon drawn.  
  -  The Player must be a lower than a specific distance set by a global variable - this is slightly more complicated and we can cover it in a later lesson. Suffice to say the Player must be relatively close to the NPC to trigger this perk.
  -  The next two are a little weird as well: they both essentially say the Subject must have a Holdup Actor Value equal to 0. Don’t worry about this, these are handled by Script Fragments in the vanilla game.  
  -  The NPC in question is NOT dead.  
  -  The NPC in question has the ActorTypeAnimal keyword.  
  -  The NPC in question does NOT have the ActorTypeDogmeat keyword.

Alright, so that’s a lot to swallow, I know. To put it a little more simply:  
**This perk only works on living animals that are not Dogmeat when you aim at them from a certain distance away.**  
Let's look really closely at those conditions in this context:  
**This perk only works on living** `[Subject.GetDead=0]` **animals** `[Subject.HasKeyword(ActorTypeAnimal)=1]` **that are not Dogmeat** `[Subject.HasKeyword(ActorTypeDogmeat)=0]` **when you aim a weapon at them** `[PlayerRef.GetInIronSights=1]` **from a certain distance away** `[Subject.GetDistance(PlayerRef<holdupDistanceGlobal)]`.

Still with me? Man, I hope so. Conditions are so important, and they largely rely on Keywords - like the ActorTypeAnimal one mentioned above. Without that one Keyword in there, you could use this perk on basically any NPC that isn’t Dogmeat...and that kind of defeats the whole purpose of it being called **Animal Friend**, right?

Now that I’ve likely confused the ever-loving shit out of you, let’s have a look at a much, much simpler one. Head back to the top of your load order in xEdit and find `Lively’s Keyword Resource`. It is ESM-flagged so it is very near the top. Expand it to see the only category: Keywords. How appropriate! And HOLY SHIT THAT’S A LOT OF KEYWORDS.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords14.png)  

So, what do these do? Well, that’s incredibly simple, because they all do the same exact thing: Recipe Filters. Every single one of them. Go ahead and click the first one, let’s see what’s in there.

Again, not much data. Type: Recipe Filter, that’s self-explanatory. The FULL - Name field is the name of the filter in-game. And...well, that’s it. That’s all this is. Click the Referenced By tab at the bottom.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords15.png)  

You’ll see here they are all COBJ records - Constructible Objects. Double click the first one.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords16.png)  

Scroll all the way to the bottom. You’ll see the BNAM and FNAM here: these tell the game where EXACTLY this Cobj can be crafted. In this case, in the Clothing Workbench under a category called `OUTFITS - OTHER`.  You may also notice that the BNAM and FNAM are both Keywords! They’re everywhere! Such versatility! It’s almost like they handle damn near everything that happens in your game! Because...well, they kind of *do*.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords17.png)  

Earlier, I promised we would make a Keyword for ourselves, so let’s do that now.

Head back to `Lively’s Keywords Resource`, right-click the `Keyword` category, and select `Add > KYWD - Keyword`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords18.png)  

The default FormID here is totally fine. Just click OK.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords19.png)  

Now we have this here blank record. How useless! Let’s put some information in here that the game can use. Right click `EDID - Editor ID` and select `Add`. Right click it again and select `Edit`, OR click it twice...slowly. Slow enough to not be a double click. Either method works.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords20.png)  

Make up a filter for something we can use - remember, it is easiest to name everything you do with a custom prefix, so that you can easily filter for it and find it later on. See how mine are all named `lkr_`? Make up a prefix for yourself - something the vanilla game doesn’t use - and stick with it.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords21.png)  

Next, edit the `FULL - Name` field. Don’t forget to right click and Add a new entry, otherwise the field literally doesn’t exist for you to edit yet.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords22.png)  

For the other bits, we’ll take a bit of a shortcut. Control-click your newly created Keyword record, as well as the one above it. You’ll see them both side-by-side in the right pane now.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords23.png)  

For the `CNAM - Color` and `TNAM - Type` fields, just drag and drop the information from the first record into your new one. This is just a bit faster than doing it manually.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords24.png)  

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d376c3a7e0475bf9c89a10863f698a50a5014303/images/keywords25.png)  

Now you can apply this new Keyword to any Cobj you like - or any workshop crafting menu, if you prefer - and the Cobj recipe in game will now appear under the `FULL - Name` you chose earlier instead of wherever it is now...as long as it has Lively’s Keywords Resource.esp as a master file. Good times!  

Hope you learned a bit about Keywords here today. See you next time.
