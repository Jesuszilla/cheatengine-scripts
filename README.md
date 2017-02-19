# CheatEngine Scripts
This repository contains various scripts made for CheatEngine, mostly to grab fighting game data.

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
