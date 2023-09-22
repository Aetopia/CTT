# Halo Infinite
This article with cover on how to optimize Halo Infinite.

??? warning "Platform Specific Optimizations"
    Halo Infinite is both available on:<br>
    <ul>
    <li>Steam</li>
    <li>Microsoft Store</li>
    </ul>
    Because of this some optimizations might be either specific to the Steam or Microsoft Store version of the game.

## Removal of High Resolution Texture Packs
??? info "Supported Platforms"
    - [x] Steam
    - [x] Microsoft Store

The High Resolution Texture Packs ship with the game are know to cause stuttering & performance issues.

1. On the title screen, go to the Control Panel.
2. Select "Manage Game" from the Control Panel.
3. Make sure the only thing that is select is the Campaign, if you own it.
4. Finally hit <button>**[Apply]**</button> to apply the changes.

![ingame-dlc](../assets/images/games/halo-infinite/ingame-dlc.png)

## Aggressive Dynamic Resolution Scaling
We may abuse the `Minimum Framerate` option for better performance.
By setting the value to `960` FPS, dynamic resolution scaling becomes insanely aggressive providing noticable performance gains.

1. Open the `SpecControlSettings.json` file depending on your platform:<br>

    |Platform|Filepath|
    |-|-|
    |Steam|`%LOCALAPPDATA%\HaloInfinite\Settings\SpecControlSettings.json`|
    |Microsoft Store|`%LOCALAPPDATA%\Packages\Microsoft.254428597CFE2_8wekyb3d8bbwe\LocalCache\Local\HaloInfinite\Settings\SpecControlSettings.json`|

2. Set the following key-value pair to the following:<br>
    ```js
    "spec_control_minimum_framerate": {
        "version": 2,
        "value": 960
    },
    "spec_control_target_framerate": {
        "version": 1,
        "value": 960
    } 
    ```

3. Here are the results for:<br>
    - 1920 x 1080
    - Low Settings (Including Settings that may be turned off.)

    ??? image "No Minimum Framerate"
        ![No-Min-FPS](../assets/images/games/halo-infinite/No-Min-FPS.PNG)
    ??? image "Minimum Framerate"
        ![Min-FPS](../assets/images/games/halo-infinite/Min-FPS.PNG)

## Visual Quality Tweaks
### NVIDIA
If you are having an NVIDIA GPU, you may avail the following techonlogies to improve visual quality.<br>
1. NVIDIA Image Sharpening
2. NVIDIA Image Scaling
3. Negative LOD Bias




