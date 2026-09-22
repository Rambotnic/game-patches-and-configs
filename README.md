# Game Patches, Fixes and Configs

> [!NOTE]
> The configuration files in this branch are meant to be used with **Linux**. For Windows, check the [windows](https://github.com/Rambotnic/game-patches-and-configs/tree/windows) branch.

This repository contains configuration files and patches for *most* of the games I own. Such files may include personal keybindings, graphics settings, mouse sensitivity settings, etc.

These settings were tested on PC:
* **OS:** Fedora KDE 44 (64-bit)
* **Motherboard:** Gigabyte Z590 AORUS ELITE ATX LGA 1200
* **CPU:** Intel Core i7-11700KF 3.6 GHz (5.0 GHz Max)
* **GPU:** MSI GeForce RTX 2060 6 GB VENTUS
* **RAM:** Corsair Vengeance 32 GB DDR4-3600 MHz (2x16 GB)

## Compatibility tools
Most of these games were tested with [Proton-CachyOS](https://github.com/CachyOS/proton-cachyos) and [Luxtorpeda](https://codeberg.org/luxtorpeda/luxtorpeda). For convenience, I recommend using [ProtonPlus](https://github.com/Vysp3r/ProtonPlus) to install them.

## Folder names and structure
The structure assumes that you're familiar with Steam's folder path.
* **NATIVE:** `<Your Steam Library Folder>/steamapps/common/<Game Name>`
* **PROTON:** `<Your Steam Library Folder>/steamapps/compatdata/<Game ID>`

Some folders may contain `[UPPERCASE_CONSTANTS]` in their names. These correspond to:
* **[$HOME]**: `/home/<Your Username>`
* **[PROTON_PREFIX]**: `<Your Steam Library Folder>/steamapps/compatdata/<Game ID>/pfx`
* **[STEAMUSER]**: `<Your Steam Library Folder>/steamapps/compatdata/<Game ID>/pfx/drive_c/users/steamuser`

## Mods, patches and source ports
Have a look at [this file](./MODS_AND_PATCHES.md) for a full list of mods and other patches.

## Steam launch parameters
To use these: right click the game > Properties > Launch Options

<details>
<summary><b>Assetto Corsa Competizione</b></summary>

**Compatibility Tool:** Proton-CachyOS Latest
```
__VK_LAYER_NV_optimus=NVIDIA_only __NV_PRIME_RENDER_OFFLOAD=1 __GLX_VENDOR_LIBRARY_NAME=nvidia PROTON_NO_WM_DECORATION=1 PROTON_ENABLE_WAYLAND=1 PROTON_USE_NTSYNC=1 gamemoderun %command%
```

</details>

<details>
<summary><b>Automobilista 2</b></summary>

**Compatibility Tool:** Proton-CachyOS Latest
```
__VK_LAYER_NV_optimus=NVIDIA_only __NV_PRIME_RENDER_OFFLOAD=1 __GLX_VENDOR_LIBRARY_NAME=nvidia PROTON_NO_WM_DECORATION=1 PROTON_ENABLE_WAYLAND=1 PROTON_USE_NTSYNC=1 gamemoderun %command%
```

</details>

<details>
<summary><b>Half-Life (and general GoldSrc Engine games)</b></summary>

```
-novid -noforcemaccel -noforcemparms -noforcemspd -nojoy -width [MONITOR WIDTH] -height [MONITOR HEIGHT] -nomsaa -nofbo +gl_vsync 0 +fps_max [MONITOR REFRESH RATE] +fps_override 1 +rate 20000 +cl_cmdrate 106 +cl_updaterate 101
```
Replace `[MONITOR WIDTH]` and `[MONITOR HEIGHT]` with your monitor's resolution, and `[MONITOR REFRESH RATE]` with your monitor's native refresh rate.

If using Xash3D FWGS, add `-console` to enable the console.

If playing Opposing Force, make sure `fps_max` is equal or lower than 120. Anything higher will break rope physics.

</details>

<details>
<summary><b>Half-Life 2 (and general Source Engine games)</b></summary>

```
-novid -nojoy -w [MONITOR WIDTH] -h [MONITOR HEIGHT] +fps_max [MONITOR REFRESH RATE] -high +mat_motion_blur_percent_of_screen_max 0 +mat_postprocess_enable 0
```
Replace `[MONITOR WIDTH]` and `[MONITOR HEIGHT]` with your monitor's resolution, and `[MONITOR REFRESH RATE]` with your monitor's native refresh rate.

</details>
