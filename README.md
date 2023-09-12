# CheatEngine Scripts
This repository contains various scripts made for CheatEngine, mostly to grab fighting game data.

## General Usage
1. Boot the game in the necessary emulator (DEmul, PCSX2, Kawaks, etc.).
2. Open the CheatEngine table (.CT file) for the respective game (after the match has loaded for best results).
3. Click "yes" when it asks to run the Lua file.
4. A window should pop up with a button that says "Start Diagnostics." Click the button.
5. Select the object you wish to observe.
6. You should now be able to view hitboxes and other data for the selected object.

All data in the window is presented in 240p (M.U.G.E.N standard). To view raw data, refer to the table.

### Caddie Machine Mode
Caddie Machine logs all animation data in M.U.G.E.N's .AIR format as the game plays, with the in-game sprite numbers used for sprite index values. So for instance, if the in-game sprite number is 326, then the corresponding M.U.G.E.N SFF value would be Group 0, SpriteNo 326 (0,326).


This logs timings in the current running game speed, so timings may not always be consistent due to Capcom's Turbo frameskipping. To get normal timings, you must set the game speed to Normal. In VSav and SFA3, you must do this in the options menu, as the Normal selectable in-game by default is actually Turbo 1.


It does not split animations, so you are responsible for keeping track of when animations begin and end.

## CvS2/CFJ
This script contains hitbox and data displays for CvS2 for PCSX2 r5875. It also works on CFJ.

### FAQ
Q: What game versions does it work on?

A: CvS2 (PS2): NTSC-U, NTSC-J. CFJ (PS2): PAL, NTSC-U. If you have a need for a different version of the game, feel free to erm... point me in the right direction ;)

Q: Do you plan for Dreamcast support for CvS2?

A: Of course!

Q: Why does it slow down at the start?

A: It's looking for throw breakpoints. Throw the opponent until the Memory Viewer pops up and it should stop. This is important for getting throw hitboxes.

Q: Why don't I see any hitboxes?

A: You need to have your PCSX2 render settings set to DirectX11 Hardware or DirectX11 Software. This uses Direct3D in order to show hitboxes, so DirectX is a requirement.

Q: Why does it not work on my PCSX2?

A: At the moment, it is only compatible with PCSX2 r5875 and 1.5.0-dev. This is because this is the version I've been using for a long time, and breakpoints change in later versions. 1.5.0-dev was chosen because it first introduced emulator-based framestepping, making one feature of the tool basically obsolete (unless you want to framestep in normal speed for whatever reason).

Q: How do I view throw boxes?

A: You have to perform every throw you want to see before the script starts or it won't pick them up. Also, it only places throws on the actively selected object, so you must select the correct object from the list.

## MvC2

### FAQ
Q: What game versions does it work on?

A: At the moment, I have only tested on NTSC-U.

Q: What's with the attack box on all basic animations?

A: That is the normal throw box. For some reason, it's always active (probably so that it's always ready to detect a throw in a fast-paced game).

Q: Why does it not work on my DEmul?

A: At the moment, I have only tested on DEmul 0.57. I have no idea if this script is compatible with later versions.
