# Game Patches, Fixes and Configs
This personal repository is meant to store all configs and patches for games I really love and am still playing or would like to return to at some point.

These settings were tested on PC:
* **OS:** Windows 11 Pro (64-bit)
* **Motherboard:** Gigabyte Z590 AORUS ELITE ATX LGA 1200
* **CPU:** Intel Core i7-11700KF 3.6 GHz (5.0 GHz Max)
* **CPU Cooler:** Cooler Master Masterliquid ML240L V2 RGB
* **GPU:** MSI GeForce RTX 2060 6 GB VENTUS
* **RAM:** Corsair Vengeance 32 GB DDR4-3600 MHz (2x16 GB)
* **Case:** NZXT H510 Flow
* **PSU:** Corsair RM850x 850W Gold+ Full Modular
* **Storage:**
	* **OS:** WD Blue 500 GB NVMe M.2 (SSD)
	* **Files:** Seagate Barracuda 2 TB 7200 RPM (HDD)
	* **Games:** Samsung QVO 2 TB (SSD)

## Folder names
Each root folder represents the name of the engine, and inside each one is a folder with the name of the game made with said engine. Most of the files are configuration and keybinds, but sometimes they can include actual patches. The folder `_Unknown` contains settings from games which I do not know what engine was used.

There's also certain folders that contain complex names with brackets. Whatever files are inside of them, you must place them in the correct path inside of your computer.

**EXAMPLE:**
* idTech
	* DOOM (2016)
		* [%USERPROFILE%] [Saved Games] [id Software] [DOOM] [base]

The above example would correspond to Windows Explorer's path: `%USERPROFILE%/Saved Games/id Software/DOOM/base` for DOOM (2016)'s config files.

If the folder DOES NOT contain complex names with brackets, that means the files are stored/placed inside Steam's game directory.

**EXAMPLE:**
* Unity
	* Dusk
		* config

The above example would correspond to the following path in your computer: `<Your_Steam_Library_Folder>/steamapps/common/Dusk/config`.

## Mods, patches and source ports
Have a look at [this file](./MODS_AND_PATCHES.md) for a full list of mods and other patches.

## Steam launch parameters
To use these: right click the game > Properties > Launch Options

- **AMID EVIL**
```
-nosplash -USEALLAVAILABLECORES -heapsize 2097152
```
<br/>

- **BioShock**
```
-nointro
```
<br/>

- **DOOM**
```
+set com_skipIntroVideo 1 +set r_skipFog 1 -USEALLAVAILABLECORES -heapsize 2097152 -sm4
```
<br/>

- **DOOM 3**
```
+set g_fov 120 +set g_gunX -2 +set g_gunZ -0.5 +set r_fullscreen 1
```
<br/>

- **DOOM 64**
```
-skipmovies
```
<br/>

- **Half-Life** (and general GoldSrc Engine games)
```
-novid -noforcemaccel -noforcemparms -noforcemspd -nojoy -width [MONITOR WIDTH] -height [MONITOR HEIGHT] -nomsaa -nofbo +gl_vsync 0 +fps_max [MONITOR REFRESH RATE] +fps_override 1 +rate 20000 +cl_cmdrate 106 +cl_updaterate 101
```
Replace `[MONITOR WIDTH]` and `[MONITOR HEIGHT]` with your monitor's resolution, and `[MONITOR REFRESH RATE]` with your monitor's native refresh rate.

If using Xash3D FWGS, add `-console` to enable the console.

If playing Opposing Force, make sure `fps_max` is equal or lower than 120. Anything higher will break rope physics.

<br/>

- **Half-Life 2** (and general Source Engine games)
```
-novid -nojoy -w [MONITOR WIDTH] -h [MONITOR HEIGHT] +fps_max [MONITOR REFRESH RATE] -high +mat_motion_blur_percent_of_screen_max 0 +mat_postprocess_enable 0
```
Replace `[MONITOR WIDTH]` and `[MONITOR HEIGHT]` with your monitor's resolution, and `[MONITOR REFRESH RATE]` with your monitor's native refresh rate.
<br/>

- **Half-Life: Alyx**
```
-novid -console -vconsole -nowindow +vr_fidelity_level_auto 0 +vr_fidelity_level 2 +vr_msaa 2 +vr_fxaa 0 +hlvr_continuous_normal_speed 110 +hlvr_continuous_combat_speed 135
```
<br/>

- **Quake**
```
+g_showintromovie 0
```
If using Ironwail, add these commands instead: `-fitz -sndspeed 44100 -heapsize 1024000`
<br/>

- **Return to Castle Wolfenstein** (using iortcw)
```
+seta r_mode -2 -console
```
<br/>

- **Wolfenstein The New Order**
```
+set com_skipIntroVideo 1 +set com_allowConsole 1 +cvaradd r_skipPostProcess 1 +cvaradd r_skipFog 1 +cvaradd r_skipFlares 1 +cvaradd r_skipSunFlares 1 +cvaradd r_skipGodRays 1
```
