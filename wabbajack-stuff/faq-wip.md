## Magnum Opus Frequently Asked Questions

---

#### **My characters have black/brown/tan/bugged faces. What happened?**

First, ensure you do NOT have the High Definition DLC active in Steam. If you don't, then quite frankly, the so-called "Black Face Bug" can happen randomly. Saving and reloading should fix it.

---

**I am having random crashes. What do I do?**

Buffout 4 generates crashlogs for you in the `\Documents\My Games\Fallout4\F4SE` folder. These are vital to diagnosing the problem.
  -  *If you don't have crashlogs here after your game CTDs, you did not follow the Game Folder Files step in the Installation instructions.*

If your crashlog references `nvwgf2umx.dll` a bunch of times, that's an Nvidia Driver crash. Downgrading to pre-445 drivers will fix this. 442.74 versions seem preferable. [Here's a link for you\(https://github.com/keylase/nvidia-patch/tree/master/win).

If your crashlog references `BGSSaveLoadManager` frequently, or `usvs::hook_DeleteFile`, or both, you are most likely running BitDefender. [Here's a link to help with that](https://www.bitdefender.com/consumer/support/answer/28557/).

Barring those two reasons, there are still a plethora of other reasons. [Auto Scanner](https://www.nexusmods.com/fallout4/mods/56255) can catch a ton of these. It is recommended you run your crashlog through this script (it's easy, you copy and paste the file, double click a thing, and press a button - no special knowledge required) and check the results.

After all that, feel free to upload your crashlog to me on [Discord](https://discord.gg/yABEjwB).

---

**How do I uncap my FPS?**

In Mod Organizer, find the `High FPS Physics Fix` mod. Double click it. In the pop-up window, select the `INI Files` tab, then select the only INI listed. In the right pane, scroll down about halfway until you see `InGameFPS=58`. Change the `58` to `0`.

---

**How do I edit the volumes for things like radios and voices?**

While in game, press Escape, then select `Mod Config`. Scroll down to the section entitled `Persistent Volume Sliders`. Adjust to your liking.

---

**I hate the HUD overlays while I'm in Power Armor. Can these be safely disabled?**

You can use the Power Armor HUD Switcher holotape to disable them. Do not disable them while you're in Power Armor. I repeat: DO NOT disable them while you're in Power Armor.

---

**Why is there a crosshair on my Pip-Boy?**

A small side effect of the Power Armor HUD overlays. You can turn the Power Armor HUD Switcher holotape setting for `Hide Hud in Pipboy` to `Off` in order to hide the crosshair when not in Power Armor, but this also makes the Pip-Boy look pretty terrible when using it inside Power Armor. Your call.

---

**Can I have multiple companions at the same time?**

[Heather Casdin](https://www.nexusmods.com/fallout4/mods/23273) doesn't occupy a "follower" slot, so you can have Heather + one other companion. You cannot have multiple vanilla companions with you at the same time.

---

**Why does my flashlight have a faint red ring around the edges?**

Because I like it.

---

**Can I add an ENB?**

If you hate yourself, sure. Some people have added ENBs and reported consistent crashes, so your mileage may vary. Don't add an ENB and report bugs to me because I can't/won't help.

---

**Why am I invulnerable/invincible/not taking damage/in permanent God Mode?**

You need to enter and exit workshop mode.  Also, please read the Magnum Opus Beginner's Guide terminal outside Vault 111. It even has a holotape version so you can read it on the go or easily reference it as needed.

---

**I am experiencing the Zero Health Bug. Healing kills me/I can't increase my health/radiation kills me/etc. What happened?"*

Unfortunately I've not experienced this myself so I can't do proper testing. From what I can gather, your health was changing (from food, drugs, radiation, etc) when you entered Workshop Mode, and now your health can't be updated by the game properly. Sometimes the `player.resethealth` console command can fix this, but I would strongly encourage you to simply load a save from before it happened.

---

**Does Magnum Opus have Ultrawide Support?**

No. I don't own an Ultrawide monitor. Some of the other people playing this list do, and one of them [wrote this guide](https://docs.google.com/document/d/1EbZ_DpyhctsrpBlylDYc2TXtm1NAOjkcYjRCNZsC958/edit) for their own Ultrawide setup. I make no guarantees on how accurate or up-to-date this information is, and I cannot help you troubleshoot any issues that arise from using an Ultrawide.

---

**I'm having problems downloading a few files, how do I fix it?**

The most common files that fail to download through Wabbajack are as follows:
  -  [Tattoos Collection by Dreivor Overlays Edition (TCD)](https://www.nexusmods.com/Core/Libs/Common/Widgets/DownloadPopUp?id=232053&game_id=1151iles)
  -  [More Hairstyles - Beards](http://www.mediafire.com/file/iztz7iidy6djz1e/MoreHairstyles-Beards.rar/file)
  -  [Misc Hairstyles 1.6](http://www.mediafire.com/file/kfac38dni6d53rp/MiscHairstyle1.6_by_Atherisz.7z/file)

Download these files manually, paste them into your `downloads` folder that you specified for Wabbajack, then rerun the installation.

---

**My loading screen is bugged/not working/etc. What's wrong?**

Nothing. The loading screens have been reduced to the bare necessities in order to allow the game to load the next area faster, instead of wasting time working on loading the loading screen.

---
