# MA3_StartShow
My custom grandMa 3 StartShow file.

The modifications I have made to the start show are:

* Compact Position Picker, with Go Button to all move at once. (Updated Position Preset Macro, to Include Low/Mid/High Positions.
* Compact Gobo Picker (same page as Positions), with Go Button for Zoom, Focus, Gobo, Animation and Iris Small.
* Color Picker Presets, Find a Color combination you want and save it to a recallable Preset. Create your Color look, and then tap the 'Store Color Preset' button, next tap on one of the 20 Color Preset Buttons on the Layout View then name it.
* Advanced Position Phaser Engine! Two Seperate Phaser Faders, you can Select Which Groups you want to have in the Faders with: Phaser Form, Groups, Blocks, Wings, Phase and Selection Shuffle.
* Advanced Color and Dimmer Phaser Engine! Select which groups you want to have in the Phaser Fader with: Form, XGroups, XBlocks, XWings, Phase and Selection Shuffle.

Things Currently on my radar to improve: 

* Part of the Position Preset Macro that asks for your Pan and Tilt Limits (-35 Thru 35 Pan, -10 Thru 100 Tilt Etc.)
* A macro that makes your Base Groups (Linear/Odd/Even).
* A focus macro that does your (Small/Mid/Wide)
* Group Intensity Faders change color depending on what color is set from color picker.

# Updates/Fixes

## v0.1.2
* Finished Position Phaser Phase Invert Macros and Updated Position Phaser Layout view.
* $MAStart_PositionPhaser1XPhaseTo/XPhaseFrom are now defined and controlled by the Phase Invert Macros.

## v0.1.1
* Fixed the Position Phaser 1 macros to correctly set the Position Phaser 1 Variables. 
* Started working on the Position Phaser Invert macros to properly define the $MAStart_PositionPhaser1XPhaseFrom and $MAStart_PositionPhaser1XPhaseTo in the global variables as this doesn't currently exist, except for being manually defined.

## v0.1
* Intial Release

# Usage

You Patch your fixtures the same as the exisiting start show, and build your groups the same. You need your fixtures to be put in their roughly correct 3D position as on the StartShow Update Layout view there is a new group for the Phaser Grid Selection which is an overall Grid selection of your Fixtures from the Top Down Perspective. You'll also need to store the Full Linear selection into the Phaser Linear Group.

# Support
Head on over to the MA Users Discord for support for this Showfile - https://discord.gg/bdxy9MtsqY

# Screenshots

![Position_Gobo Picker](https://github.com/user-attachments/assets/e137d857-f0b3-492c-8de5-a4d1dcb66fee)

![Colour Picker](https://github.com/user-attachments/assets/dad0861a-f4f5-44bd-baea-9181ff9ccf24)

![Position Phaser Picker](https://github.com/user-attachments/assets/2da58a0f-6ecd-4252-aa15-3ddfb593650e)

![DIM_COL Picker](https://github.com/user-attachments/assets/580d673c-29ce-470f-9e0c-40e787cbbc47)

![Fader Page](https://github.com/user-attachments/assets/35f808a4-dde5-4158-b269-a1bf18473f47)
