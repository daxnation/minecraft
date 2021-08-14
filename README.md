# Minecraft!

## Minecraft Mods
In this section you can find a couple of mods that you can apply to Minecraft to expose some additional performance and visual tweaks (OptiFine) and some texture packs that Garak (and maybe others!) are using that have little to no performance impact.

### Setup OpenJDK
Java is required for installation of this mod and others. If you already have official Oracle Java installed on your computer, you can skip this guide and move onto installing Mods. The Oracle Java runtime now has strict licensing requirements and is often more insecure than the open version (in my opinion), so this guide will walk through downloading the latest version of OpenJDK from the Eclipse group's Adoptium Project.
  1. Navigate to the [Adoptium release download page](https://adoptium.net/releases.html).
  2. At step 1. under version, select `OpenJDK 16 (Latest)`.
  3. Find the Windows version (or select Windows from the `Operating System` drop-down) and then select the `.msi` file download.
> ![](https://raw.githubusercontent.com/daxnation/minecraft/main/guide_pictures/setup_openjdk/Adoptium_release_page.png)
  4. Run the installer to install OpenJDK. The defaults should be fine and should add the appropriate settings to run Java from the command line.
> ![](https://raw.githubusercontent.com/daxnation/minecraft/main/guide_pictures/setup_openjdk/JDK_Setup_Options.png)
  5. Finish the installation.

### Install Iris Mod
The Iris Mod bundles custom routines and a custom fork of the Sodium renderer for tons of performance and high mod compatibility. This guide will walk through installing Iris as a Fabric mod (using the Iris installer).
  1. If you haven't done so already, open the Minecraft Launcher and run your current installation of Minecraft. You can quit once it gets to the main menu.
  2. Navigate to the [Iris Download Page](https://irisshaders.net/download.html) and click `Download Universal Jar`.
  3. Open the folder where Iris Mod was just downloaded.
  4. Hold the shift key and right click in any blank space of the window; then click `Open Command Prompt Window Here` or `Open PowerShell Window Here` depending on your version of Windows.
  5. Type the command `java -jre name_of_file.jar` and hit enter to run the installer. For example, `java -jar Iris-Installer-2.0.0.jar`.
  6. On the window that opens, select your current game version (1.17.1 as of this writing) and check `Install as Fabric Mod`.
> ![](https://raw.githubusercontent.com/daxnation/minecraft/main/guide_pictures/iris_mod/Iris_Installer_Options.png)
  7. Click `Install` and the mod install will run. The progress bar will hit 100% and say `Installation complete!`
  8. Close the install and your cmd or Powershell window.
  9. Open the Minecraft Launcher and, if it is not already, select the Fabric 1.17.1 (or your current version) installation and then click Play.
> ![](https://raw.githubusercontent.com/daxnation/minecraft/main/guide_pictures/iris_mod/Minecraft_Launcher_Iris.png)
  10. You will get a warning about running modified content, check the box and click Continue (or play, I didn't get a chance to grab a screenshot).
  11. Connect to the Minecraft server and once loaded in, hit `F3` to bring up performance metrics. You should see `Iris Version: X.X.X.X` on the right side of the screen towards the middle.
> ![](https://raw.githubusercontent.com/daxnation/minecraft/main/guide_pictures/iris_mod/Minecraft_F3_Screen.png)
  12. Enjoy your free extra performance!

### Installing Fabric Mods
  1. Now that Iris is installed as a Fabric mod, I strongly recommend installing these two mods, [Fabric API](https://www.curseforge.com/minecraft/mc-mods/fabric-api) and [Mod Menu](https://www.curseforge.com/minecraft/mc-mods/modmenu). The former is required for many Fabric mods (including Mod Menu) and the latter adds a menu to Minecraft that shows all of the installed and running mods.
  2. Once you download these mods, open a `Run` dialog box either by hitting `Win+R` on your keyboard or right-clicking the Start Button and clicking `Run`.
  3. In the Run box, enter the text `%appdata%\.minecraft\mods` and click OK.
> ![](https://raw.githubusercontent.com/daxnation/minecraft/main/guide_pictures/iris_mod/Run_box_to_mods.png)
  4. Copy the `.jar` files for these two mods to the folder that you've opened. You should already see the Iris mod file in this directory.
> ![](https://raw.githubusercontent.com/daxnation/minecraft/main/guide_pictures/iris_mod/Mods_Folder_Example.png)
  5. With the Mods in the `mods` folder, open up the Minecraft launcher and then the Fabric install of Minecraft.
  6. Once Minecraft opens, if the installation was successful and you installed Mod Menu, you will see this addtional menu option present and can look at your installed mods.
> ![](https://raw.githubusercontent.com/daxnation/minecraft/main/guide_pictures/iris_mod/Minecraft_with_Mod_Menu.png)
  7. Most Fabric mods are installed using this method. Any new mod will require restarting Minecraft (if installed while the game is running).
  8. Here is an example of Mod Menu with several Fabric Mods installed!
> ![](https://raw.githubusercontent.com/daxnation/minecraft/main/guide_pictures/iris_mod/Mod_Menu_Example.png)

### Recommend Fabric Mods
I have installed several mods that aim to increase performance in Minecraft along with Iris. Links and descriptions below!
  - [Hydrogen](https://modrinth.org/mod/hydrogen) - This mod aims to reduce Minecraft's memory usage. I've seen a significant reduction in memory usage using this mod.
  - [Lithium for Fabric](https://www.curseforge.com/minecraft/mc-mods/lithium) - This mod makes some adjustment to a number of ingame systems to reduce their CPU usage and can help improve the game's responsiveness and framerate.
  - [Lazy DFU](https://www.curseforge.com/minecraft/mc-mods/lazydfu) - This mod significantly reduces the initial game load time by allowing Minecraft to not pre-cache any conversion routines until it needs to do so. This CAN introduce some stuttering in-game when DFU routines run, but I personally have not noticed any performance hit due to these calls.
  - [Entity Culling Fabric](https://www.curseforge.com/minecraft/mc-mods/entityculling) - This mod changes rendering behavior to stop the game from rending entities that are not currently being drawn on screen (HELLO HIGH FPS IN New DaxJacktown!). Aside from Iris itself, this has introduced by far the most noticable improvement in game performance for me.
  - [Cull Leaves](https://www.curseforge.com/minecraft/mc-mods/cull-leaves) - This mod does the same as above, but for leaves. It basically mimics the "Smart" settings for trees available in OptiFine. Some users report that this can change the look of leaves, but if it does I have not been able to tell. (This mod also needs to be turned on in the `Options... -> Resource Packs...` menu as well to be activated.)
  - [LamDynamicLights](https://modrinth.org/mod/lambdynamiclights) - This mod add dynamic lights to the game so if you are holding a light source, it lights up. This frees you from having to use a shader that adds dynamic lighting and makes it global instead if you're just after high framerates!
