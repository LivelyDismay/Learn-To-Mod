## What are Collections?

Collections are a new project by NexusMods. It acts as an automatic modlist installer. In layman terms, one person makes a personal modlist, then has the ability to share that modlist with others via uploading machine-readable instructions that others can use to replicate the installation of that modlist on their own PCs.

## How did I get here?

Collections have been in closed testing for a few months now. As we expand the testing pool to get more and more feedback, the Nexus has reached out to frequent users of the site, inviting you to participate in testing this project.

## How do I access Collections?

Join the Discord server you were sent an invitation to on NexusMods and read the #how-to-get-started channel. This will give you a quick rundown of what Collections are, how to use them, what they're capable of, and how to access some Collections that are ready to go.

## Building a Collection: What are the limitations?

There's really only one primarily limitation: you cannot under any circumstances directly edit files inside your installed mods. Any direct edits to mods cannot be automated, and must be done manually by the user.

## Building a Collection: How do you handle FOMOD installers?

In your Collection Workshop on Vortex, you'll see a dropdown menu with three options next to each mod:  
  -  **Fresh Install**: Acts as if the user just installed the mod themselves. The FOMOD opens and they can choose whatever options they want.  
  -  **Same Installer Options**: Acts as if the user just installed the mod themselves; however, the FOMOD's pre-selected options will be set to the options the Collection Curator chose during their own installation.  
  -  **Replicate**: Bypasses the FOMOD entirely. Instead of installing the mod normally, Vortex will check your installed mod, read what files are inside, then find the relevant source archive tied to the mod. Once Vortex opens that archive, it will simply move the files from the archive into the mod folder to match how the Collection Curator has it set up on their end.

## Building a Collection: Can you use files that aren't hosted on Nexusmods?

Absolutely! In the Collection Workshop on Vortex, you'll see another dropdown next to each individual mod with the following options:  
  -  **NexusMods**: The one you'll most likely be using for a majority of your mods, this states that the mod is from Nexusmods.com.
  -  **Direct Download**: Provide a link for Vortex to download the file directly. Rather self-explanatory. Useful for things like MEGA links.
  -  **Browse a Website**: Enter a URL which Vortex will open for the user installing the Collection. Be sure to include instructions on exactly what to click on and what to download so users can get the correct file needed.
  -  **Bundle With Collection**: Inlines the file into the Collection upload itself. This can only be done for files you have permission to distribute, such as plugins you own or created yourself.

## Building a Collection: How do I include Script Extender?

Download Script Extender like you normally would. In the Collection Workshop, set the mod to Browse a Websiteand enter in the URL for the silverlock website, along with instructions on which link to click on.

Once Script Extender is installed, navigate to your `Mods` tab in Vortex and Enable the script extender mod. Double click it and change the Mod Type to `Engine Injector`.

## Building a Collection: What do I do with patches I've created for the Collection?

Patches you've made can be bundled with the Collection, or even hosted on Nexusmods for others to use as standalone patches. Entirely up to you how you want to handle that.

## Building a Collection: How do I handle tweaked .ini settings?

For the base game ini files, you can use the `INI Tweaks` tab in Vortex's Collection Workshop.  
For mod-added ini files, leave the original INI file in the mod untouched. Make a copy of it and paste it into a new mod, then edit it to your liking. When you're done, bundle that new custom mod with the Collection. This way, the source is still being used, and your edited INI file will load after the original, thus overwriting it.

## Testing Collections: Can I install multiple Collections?

You sure can. You can even install multiple Collections in the same profile in Vortex.  **Please be aware**, however, that this is not useful for testing. Collections contain dozens or even hundreds of mods. There is no guarantee that any Collection will work with another Collection without some extremely thorough patching.

## Testing Collections: Can I add mods to a Collection?

Yes, but again, this completely defeats the purpose of testing the Collections feature. We want you to have fun, of course, but we are currently looking for feedback on both how to improve Vortex/Collections, and how to improve the currently existing Collections. If you add mods and subsequently encounter issues with your game, we simply can't know if the problem is because of the mods you added or not, and so your feedback becomes completely worthless.

## Testing Collections: What do I do if something is wrong with the Collection I downloaded?

Good news: this is exactly why you're here! Nexus staff is looking for any and all problems with Collections, no matter how big or small. There are a few avenues you can take:  

1. If Vortex failed to install or seems to be throwing an error, you can use the Report button in Vortex itself. This will notify the Vortex developers and send them all the necessary information they need, all at the click of one button from you.  
2. If the Collection itself has some errors, such as unresolved conflicts or missing masters for example, get in touch with the Collection Curator on the Nexus Next discord server. If the curator states that those conflicts/masters/etc are resolved on their end, then this means Vortex encountered some sort of error during installation, at which time you should notify the Nexus staff of your issues.

Remember: this is a team effort. We all need to work together to make Collections the best they can be prior to a full release.

