# Yi Chuan CRT Board
Schematic and other info about the Yi Chuang CRT replacement board from 2023. Has a ton of customizability!

Now, first off, this board cannot be modified to add a RGB input. The Main IC does not support that. It can be modified to support S-Video and Component video -- and we are working on those details. 

* Toshiba 8873CSCNG6PR6 is the datasheet for the main IC used on this CRT board
* "Chinese TV Board combined" are the schematics, scanned by me
* "Specs" are from the side of hte box that my board was inside

----

To access the service mode, push the little secret button on the remote below the SCAN button. You will need a pen or paperclip to push it.

First push you get FACTORY displayed at the top. Second push you end up F0, which allows you to setup the RGB Drive and CUT. While on F0, push the SLEEP button to cycle through built in test patterns.

Push the service button again and you will see F1. This allows you setup the size,deflection,etc for the CRT. 

Push the MUTE button to display F2. At the bottom, you will see PAGE 0. Go down to this (using up/down) and push left/right to change to 1.

Now continue to push MUTE button to cycle through all service mode screens, F1 through F18.

I recommend these settings to make this a better NTSC monitor. It's way too bright.
F2 SUB CONT -> 2
F2 SUB BRI -> 3
F2 SUB.COLOR -> -29
F2 OSD CONT -> 2

To fix the mis-adjusted NTSC tint, so it's accurate when the menu tint is set to +/-0:
F16 -> TNTC -> 66 (originally 53)

Now in the picture settings, you set set it to:
CONTRAST 50
BRIGHTNESS 50
COLOR 50
TINT +/- 0
SHARP 50

To allow the TV to tune in NTSC RF channels properly:
F4 M -> 1 (this makes it so the 4.5mhz audio spacing works)

To improve the Composite video performance on NTSC:
F14 CTRPQ -> 1 (originally 0)
F13 CVBS.PASS -> 1 (originally 0)

F18 S.SYS -> AV (this allows you to setup the delay for each type of input)
then
F18 Y-DELAY 6 (this improves the luma/chroma sync on NTSC at least)
DEMO.PHASE 1

F18 PP Mode -> You can configure the defaults for the various picture modes. They are all terrible so I recommend 50/50/50/50 for a good baseline, then I have one called MILD which is good for using the set with 8-bit computers like the Apple II. Another profile for color turned to zero, etc.

F3 LOGO is the boot screen. I have mine on 2, it makes it red background. 
F3 No.SG.LOGO set to 2 as well for the bouncing mini logo when no signal
F3 DSP POSITION -> 0 or 1 (moves the channel/input display to the left corner)

F6 has a bunch of languages listed, you can disable all of the ones you don't want. (I disabled everything but English)

F7 ICON COL -> 0 (this will hide the menu icons entirely, since the yare useless anyway)
F7 MENU BACK -> 3 (will give the menu a nice background to make it more readable)





