# GTA Remix Fixes
An .asi modification for GTA games to make them compatible with RTX Remix(currently from Portal RTX)

Download: https://github.com/dports/gta-remix-compat/releases/download/v1.0/remix_compat.asi

## How to build:
1. Install scoop.sh and Visual Studio 2022
2. Install Experimental v143 C++ Modules
3. ```scoop install vcpkg```
4. ```vcpkg install wil:x86-windows-static```
5. ```cmake . -DCMAKE_BUILD_TYPE=RelWithDebInfo -DCMAKE_TOOLCHAIN_FILE=%USERPROFILE%\\scoop\\apps\\vcpkg\\current\\scripts\\buildsystems\\vcpkg.cmake -DVCPKG_TARGET_TRIPLET=x86-windows-static -A Win32```
6. ```cmake --build . --config RelWithDebInfo --target remix_compat```

## How to use:
1. Install ASI Loader
2. Install RTX Remix
3. Drag-n-drop asi file to game folder(be sure to read ASI Loader Readme file beforehand, sometimes it doesn't load from game folder)
4. Run the game, you will still need to mark all the UI textures as such for now, but later this mod will feature configuration files
5. If you encounter reproducible bug you are welcome to report it, do be careful some bugs can't be fixed without support from NVIDIA team behind RTX Remix

## Current status
### GTA SA
- Game runs in windowed mode via [this mod](https://github.com/ThirteenAG/III.VC.SA.WindowedMode/releases/tag/v1.11)
- Can be run in fullscreen but only on low resolution
- Ambient directional lights were disabled due to incorrect lighting
- Post effects were disabled due to visual bugs
- Decals and blob/stencil shadows were disabled due to incorrect looks(Decal rendering should be fixable)
- Mirror rendering were disabled, due to bugs
### GTA VC
- Game runs in windowed mode with dxwrapper
- No specific fixes yet
### GTA 3
- Game runs in windowed mode with dxwrapper
- No specific fixes yet
