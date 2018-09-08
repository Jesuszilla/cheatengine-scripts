# CheatEngine Scripts
This repository contains various scripts made for CheatEngine, mostly to grab fighting game data.

## General Usage
1. Boot the game in the necessary emulator (DEmul, PCSX2, Kawaks, etc.).
2. Open the CheatEngine table (.CT file) for the respective game (after the match has loaded for best results).
3. Click "yes" when it asks to run the Lua file.
4. A window should pop up with a button that says "Start Diagnostics." Click the button.
5. Select the object you wish to observe.
6. You should now be able to view hitboxes and other data for the selected object.

All data in the window is presented in 320p (M.U.G.E.N standard). To view raw data, refer to the table.

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

Q: Why does it crash PCSX2 after running for a while?

A: I have no idea but it probably has to deal with the D3D hook; hopefully I can fix it. If you think you can fix it, feel free to submit a pull request!

Q: Why does it not work on my PCSX2?

A: At the moment, it is only compatible with PCSX2 r5875. This is because this is the version I've been using for a long time, and breakpoints change in later versions. I may update it soon for the latest.

## MvC2
Q: What game versions does it work on?

A: At the moment, I have only tested on NTSC-U.

Q: What's with the attack box on all basic animations?

A: That is the normal throw box. For some reason, it's always active (probably so that it's always ready to detect a throw in a fast-paced game).

Q: Why does it not work on my DEmul?

A: At the moment, I have only tested on DEmul 0.57. I have no idea if this script is compatible with later versions.