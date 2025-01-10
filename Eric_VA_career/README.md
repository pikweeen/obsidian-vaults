# How to load a mod

The mod will contain one or more `.assets` and `.resource`. The `.resource` should have unique names, but `.assets` should coincide with files inside the vanilla game folder. 

Simply **go into the `hollow_knight_Data` folder and copy and paste the mod files into it**. This will destroy your original vanilla files, so make sure to **make a backup of your `.assets`!!**
# How to make a mod

Essentially a **glorified texture pack!** I'm just calling it a mod because people call texture packs "lvl 2 mods" and I think it sounds better.
## Required programs

- **[Unity (Hub)](https://public-cdn.cloud.unity3d.com/hub/prod/UnityHubSetup.exe)** --- Pick a Unity Editor between version 2017 and 2021.3
	</br> To convert your original `.wav` to `.assets`
- **[Asset Bundle Extractor](https://github.com/SeriousCache/UABE/releases/tag/v3.0-beta1)**
	</br> To import/export dumps on `.assets`
- **[AssetStudioGUI](https://github.com/Perfare/AssetStudio/releases)** 
	</br> To navigate assets and preview their contents
- **An audio editor of your choice ([Audacity](https://www.audacityteam.org/download/))**
	</br> To create your new sounds

Assets are stored in the `hollow_knight_Data` folder in the game, **we're just touching `.assets` and `.resource` files**. Using AssetStudio you can open these `.assets` and listen to the different files.

## 1. Locate the files to be modified (AssetStudio)

You can open the main folder and that will open every asset in the game, so you can now find out the name of the specific sound or character you're looking for (go on the Asset List tab please). 

If you right-click on a file and select **`"Show original file"`** you will find out which of the 500 `.assets` it's stored in. **Remember this, it WILL come up later.** If you want to change several sounds and they're on different files, you will have to follow this process individually with each one.

Note: You can export them into `.wav` by selecting them and going on **`Export > Selected Assets`**. 

## 2. Create new sounds

This is the fun part, aren't you having fun?? Having exported the vanilla files, you should now have a hefty checklist. You can now **record yourself or your friends** to make the new assets for the game, or otherwise **find sounds online**. 

Making the new files have the same names as the vanilla ones isn't necessary but it is recommended. Just make sure they're `.wav`.

## 3. Make them into actual assets (Unity)

1. Create a **new Unity project**.
2. **Drag and drop your `.wav` files into the timeline, and then onto the scene**. Make sure to **do this separately for each `.assets`**. If the sounds you're changing are in three different files, you need to do this three times.
	</br> Don't worry about the Camera, light source etc, they won't affect anything.
1. Select `File > Build Settings` and **build the project**. Pick a good folder. This will generate `.assets` and `.resource` files with your things.
2. **Rename the `.resource` to something that identifies your mod**. You should never replace the vanilla `.resource` in the game files, because other assets may depend on it.
## 4. Fix your assets (Asset Bundle Extractor, ABE)

We need to modify something in the `.assets` to reference the new name of the `.resources`, which can only be done when the asset is in `txt` format. 
1. **Open the `.assets` with ABE, select its contents and select `Export Dump > Dump as text file`.**
2. This will generate as many `.txt`'s as new sounds you made. You need to **go in all of them and change the `m_Source` field to the exact name of the `.resource`** that Unity generated for you. Have fun.
## 5. Put your sounds into the vanilla assets (ABE)

Now that you have each of your sounds in the correct format, you can put them in.
1. **Get the `.assets` file that contains the vanilla sounds you're trying to change**. Now make a **backup** of it. *Now* open it on ABE.
2. Sound by sound, select them and then go to **`Import Dump`**, where as you may guess you **put in your new sounds** (the dumps, `.txt`).
3. **Save it into your mod folder** (NOT the game folder. I ***will*** kill you).
4. **Rename it to the vanilla `.assets`** you want to replace.

## 6. You're done!

Now you should have one `.assets` with its `.resource`. The `.assets`'s name should already exist in the game files, and the `.resource` should be some random shit you made up. Ideally one mod folder would have several.

You can follow the [How to load a mod](#how-to-load-a-mod) section to check whether it worked.

Have fun :)
