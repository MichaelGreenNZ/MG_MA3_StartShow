# MA3_StartShow

<div id="badges">
  <a href="https://www.instagram.com/MichaelGreenNZ/">
    <img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram Badge"/>
  </a>
  <a href="https://www.linkedin.com/in/michaelgreennz/">
    <img src="https://img.shields.io/badge/LinkedIn-blue?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge"/>
  </a>
  <a href="https://discord.gg/bdxy9MtsqY">
    <img src="https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white" alt="Discord Badge"/>
  </a>
  <a href="https://www.facebook.com/MichaelGreenNZ/">
    <img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white" alt="Facebook Badge"/>
  </a>
</div>

## Introduction

I liked the foundation that the MA StartShow file provided, but found there were limitations in how I wanted to Busk for the shows I work on. So I started modifying and customising small bits of the file to my liking. 

I started with the Position, Dimmer and Color Phasers as I wasn't a fan of toggling on each individual group and they just started running. I wanted more control over when they started and stopped. Taking inspiration from a Plugin I had seen from MA 2 and also Christian Jacksons MA 2 FX Macros from You Tube, I set about building A single fader per Phaser Type and adding or removing Groups of Fixtures from Those Phasers. My first attempt was clunky but functional to me, however could break with the slightest group update or preset change. So kept working on that, testing it on various rock and theatre shows that I was working on. Eventually got it to the stage of stability and not able to break it by changing anything in patch/groups/presets, Using worlds applied to the Phaser Faders and a Single Grid or Linear Select group applied to the Recipe Line and varying forms options controlled by macros.

My Next goal was a more Compact Position Picker with more Position options (Low/Mid/High) as I am often working on a MA 3 Light and wanted to reduce the amount of View changes I needed to make per Change. I also wanted to be able to select a number of position changes per each group and trigger them all at the same time either with a snap or a fade. A similar function to Giaffo Designs 'RateMaster "Go"'.

Trying to create the Color Picker Preset was a fun challenge, having to learn more about the Variables System and using multiple commands per macro line, I still think there are improvements to be made here but think the ones I want like a popup window with the Presets Highlighted for selection will be a Lua Script and perhaps not needed. I did make it that rather than having to type in the Name or Macro Number of the Preset you want to save too you can type the store color preset button and then just select the preset icon on the screen, this is done by leaving the command to store macro number to a variable in the command line, which could be of concern if you get disracted during storing a color preset, and then go to press something else, and it then keeps running the macro. So I think I'll need to create a check or something that the Variable is a Preset within a range. Probably more Lua.

The compacting of the Gobo Selector proved difficult with the implementation of the seperate zoom range across Open/Gobo 1/Gobo 2. While also making it all function with a synced go Button also. Eventually the only way was to seperate out the zoom and focus in the presets, so you have your three zoom levels, and then 14 different Focus Presets (not ideal, hopefully I can find a better way) three each for Open/Gobo 1/Gobo 2 and one each for Iris Small and Animation Wheel.

Hopefully you find this useful either in using the file for your own shows, or finding things in the macros that you can use in your own file! Feel free to link me to any of your gig photos on Instagram or via the Discord #Sscreenshots Channel. I really want to keep building on this, and am open to any suggestions so long as I am capable of doing them!

### The modifications I have made to the start show are:

* Compact Position Picker, with Go Button to all move at once. (Updated Position Preset Macro, to Include Low/Mid/High Positions.
* Compact Gobo Picker (same page as Positions), with Go Button for Zoom, Focus, Gobo, Animation and Iris Small.
* Color Picker Presets, Find a Color combination you want and save it to a recallable Preset. Create your Color look, and then tap the 'Store Color Preset' button, next tap on one of the 20 Color Preset Buttons on the Layout View then name it.
* Advanced Position Phaser Engine! Two Seperate Phaser Faders, you can Select Which Groups you want to have in the Faders with: Phaser Form, Groups, Blocks, Wings, Phase and Selection Shuffle.
* Advanced Color and Dimmer Phaser Engine! Select which groups you want to have in the Phaser Fader with: Form, XGroups, XBlocks, XWings, Phase and Selection Shuffle.

### Things Currently on my radar to improve: 

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

Head on over to the MA Users Discord for support for this Showfile - <a href="https://discord.gg/bdxy9MtsqY">
    <img src="https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white" alt="Discord Badge"/>
  </a>


# Screenshots

![Position_Gobo Picker](https://github.com/user-attachments/assets/e137d857-f0b3-492c-8de5-a4d1dcb66fee)

![Colour Picker](https://github.com/user-attachments/assets/dad0861a-f4f5-44bd-baea-9181ff9ccf24)

![Position Phaser Picker](https://github.com/user-attachments/assets/2da58a0f-6ecd-4252-aa15-3ddfb593650e)

![DIM_COL Picker](https://github.com/user-attachments/assets/580d673c-29ce-470f-9e0c-40e787cbbc47)

![Fader Page](https://github.com/user-attachments/assets/35f808a4-dde5-4158-b269-a1bf18473f47)
