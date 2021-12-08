# OMORI-2019-build-documentation
Documentation of all changes from the "leaked" 2019 OMORI build to the first release of the game in 2020

# Installing the 2019 build
If you would like to help us documenting the changes or would simply like to explore them yourself, you will first need to acquire the 2019 build files.
For that, you will need:
- A copy of [OMORI](https://store.steampowered.com/app/1150690/OMORI/)
- The latest version of [OneLoader](https://github.com/rphsoftware/OneLoader/releases)
- A text editor
- [RPG Maker MV](https://store.steampowered.com/app/363890/RPG_Maker_MV/) (Optional)

## Installing OneLoader
In order to be able to decrypt the game files, you will need to install [OneLoader](https://github.com/rphsoftware/OneLoader/releases).

Then, navigate to your OMORI folder, on Windows, it would usually be in `C:\Program Files\Steam\steamapps\common\OMORI` but it is recommended to open the folder from Steam itself. Simply right-click the game in your library, hover over *Manage* and click on *Browse local files...*

Extract the entirety of your OneLoader zip into this folder, if everything went alright, you should be prompted to replace exactly one file. Allow the replacement.

To verify if OneLoader is installed correctly, simply launch the game from Steam, it should display the OneLoader version in the top left corner of the title screen.

For a more detailed explanation on installing OneLoader, visit the [OneLoader GitHub repository](https://github.com/rphsoftware/OneLoader/).

## Downgrading to 1.0.1
The 2019 build data can be found in the 1.0.1 version of OMORI, you can downgrade to that version from Steam.

1. Right-Click on OMORI in your Steam Library
2. Click on *Properties...*
3. Navigate to *BETAS*
4. Select the beta `v1.0.1 - OMORI V1.0.1`
5. Close the properties window
6. If not done automatically, "update" OMORI

The update should not affect your OneLoader installation, if it does however, it may be needed to install it again.

## Decrypting a vanilla 1.0.1 build
In order to compare the 1.0.1 version to the 2019 build, you will need access to the decrypted 1.0.1 files.

To decrypt your game, you must have OneLoader installed as described above.

1. Start OMORI from Steam
2. Navigate to the *OPTIONS*
3. Select *MODS* then *DECRYPT OPTIONS*
4. Make sure to set *Decryption mode* to either *EVERYTHING* (if you have no mods installed) or *BASE GAME*
5. (Optional) If you have [RPG Maker MV](http://store.steampowered.com/app/363890/RPG_Maker_MV/), you may also want to enable *Generate as RpgMaker project?* to access the project file for the game. If not, you can leave it disabled
6. Click on *Start decryption*, the decryption process will take a while, but once it's done you will have a new decrypted copy of the game files in your OMORI folder

## Installing the 2019 build as a mod
To be able to play and/or decrypt the 2019 build of OMORI you will first need to create a OneLoader mod with all of its data.

The 2019 build data can be found in your regular encrypted OMORI files, navigate to `OMORI/www/img/characters/`, you should find a folder named `data`, that folder contains all of the known data about the 2019 build. Take note of its path as we will need to copy it later.

1. Navigate to your `OMORI/www/mods`, that directory should have been created upon installing OneLoader, create a new directory inside of it, you may call it whatever you want. For the purposes of this guide we will assume you have called it `2019-build`
2. Copy the previously mentionned `data` folder inside of `2019-build` so that `2019-build` only has one subdirectory called `data`
3. Create a new folder inside of `2019-build` and name it `plugins`
4. Inside of `plugins`, create a new JavaScript file named whatever you'd like. For the purposes of this guide, we will name it `decryptFix.js`
5. Inside of this new file, write 
```js
{
  let z = DataManager.onLoad;
  DataManager.onLoad = function(l) {
    if (l == $dataSystem) { $dataSystem.hasEncryptedAudio = true; $dataSystem.hasEncryptedImages = true; }
    z.call(this, l);
  }
}
```
6. Navigate to your decrypted 1.0.1 folder, then go to `data` and then open `System.json` in the text editor of your choice.
7. Scroll to the bottom of the file and locate the text reading `"windowTone":[0,0,0,0]`, you should see a few other items between that and the end of the file. Copy everything between `"windowTone":[0,0,0,0]` and the end of the file.
8. Paste what you have copied into the `data/System.json` file inside of your `2019-build` mod, in the same location as it was in the vanilla file, you can again use the string `"windowTone":[0,0,0,0]` to guide you.
9. Create a new file in your `2019-build` folder and name it `mod.json`
10. Inside of `mod.json`, paste the following (if your mod folder is not named `2019-build`, replace `"2019-build"` with the name of your mod folder):
```json
{
    "id": "2019-build",
    "name": "2019",
    "description": "Mod that contains all 2019 data known to man",
    "version": "1.0.0",
    "files": {
      "plugins": ["plugins/"],
      "data_delta": [],
      "text": [],
      "data": [ "data/"],
      "maps": [],
	  "assets": [],
      "exec": []
    }
  }
```
11. Save the file and launch OMORI from Steam
12. If everything went well, you should reach the title screen without any issues. To verify if the 2019 build is installed correctly, check the window title.

## Decrypting the 2019 build
To decrypt the 2019 build, follow the exact same steps as above for **Decrypting a vanilla 1.0.1 build** however, this time, select *EVERYTHING* or *MODS ONLY* as the *Decryption mode*

And congratulations! You now have a copy of OMORI as it was in 2019.

# How to contribute
Of course, this repository was mainly made to share finds from the 2019 build and to document them.

1. Find something of interest in the build. Make sure that it differs from the released game.
2. Fork the repo. 
3. Make your changes.
4. Make a pull request. Before doing this, make sure that your contribution abides be the appropriate template.
5. Assign the pull request to the appropriate issue.


