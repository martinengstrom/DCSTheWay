# DCSTheWay
Imports waypoints right into the plane navigation system, like a Data Transfer Cartridge.
[DCS Forums thread here](https://forum.dcs.world/topic/272110-transfer-steerpoints-from-the-f10-map-into-the-aircraft-dcs-the-way/)

## What does it do?
You choose points on the DCS F10 map, press a button, and those points will be entered as steerpoints into your plane automatically. 
You can also share those waypoints with your friends, and you will all fly the same route, regardless of the module they choose.

## What is supported?
Supported modules:
* F-16 (& All IDF Mods Project F16s)
* F/A-18 
* A-10C and A-10C2
* Mirage 2000
* AV8BNA Harrier
* Ka-50 Blackshark
* AH-64D Apache (Pilot and CP/G)

## Under Development
* F-15E S4+ (WIP)
 
Multiplayer is supported as long as the server has Player Exports turned on (most servers do).

## How to install?
1. Download the latest zip file from the Releases section, and extract it. 
2. Copy the `TheWay.lua` file from the folder you just extracted into `Users/YourUsernameHere/Saved Games/DCS/Scripts`. The `DCS` folder name may be `DCS.openbeta` if you are on the openbeta version of the game. If you are on Steam, the name will always be just `DCS`.
3. Edit the `Export.lua` file there and append this line at the end of the file, and save it:
  ```lua
  local TheWayLfs=require('lfs'); dofile(TheWayLfs.writedir()..'Scripts/TheWay.lua')
  ```
   If there is no `Export.lua` file already existing there, create it yourself, and it should include only the line above.

4. Run the installer from the zip file you've previously extracted.
5. After installation, the program will launch, and you can go fly! You can find a shortcut to TheWay on your desktop.

If you are updating from an older version, simply download the newest release, rerun the installer and replace your existing `TheWay.lua` file in Saved Games with the new one.

## How to use? 
Video tutorial here:

[![DCSTheWayVideoThumbnail](https://img.youtube.com/vi/B2Q1VurZ8ms/default.jpg)](https://youtu.be/B2Q1VurZ8ms)

## FAQ
### I have a problem with my installation
Worry not, feel free to message me on Discord (Doge#4634) or the ED Forums thread and we'll have it sorted!

### How do I use this for VR?
As I do not own a VR headset, it is hard for me to build a user interface for it. But, instead I have implemented a series of keybinds to help:
CTRL+SHIFT+S: to save a point
CTRL+SHIFT+T: to transfer the waypoints
CTRL+SHIFT+D: to delete all waypoints

## Credits
Special thanks to discord users: kukiric, Bepis, the88tench, okopanja, and the ED Forums users for their suggestions and help.

## For nerds
The application is built using React.js and Electron. If you'd like to contribute, simply clone the repository and run `npm install`, then `npm run react-start` to start the React page, and `npm run electron-dev` to fire up the Electron side of things.
If you'd like to build/package the code for production, run `npm run package` and check the `dist` folder for the created installer. 

This is the way.
