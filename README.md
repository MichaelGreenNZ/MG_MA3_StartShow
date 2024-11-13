# MG_MA3_StartShow

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

## Showfile breaking BUG with MA3 v2.1.1.5, doing a Partial Show Read will break Handle references #[] used throughout the showfile. MVR export of showfile and then import into showfile works fine!

## Current Console Version File Saved On - **2.1.1.5**

## Introduction
<details>
<summary>I liked the foundation that the MA StartShow file provided, but found there were limitations in how I wanted to Busk for the shows I work on. So I started modifying and customising small bits of the file to my liking.</summary>

I started with the Position, Dimmer and Color Phasers as I wasn't a fan of toggling on each individual group and they just started running. I wanted more control over when they started and stopped. Taking inspiration from a Plugin I had seen from MA 2 and also Christian Jacksons MA 2 FX Macros from You Tube, I set about building a single fader per Phaser Type and adding or removing Groups of Fixtures from Those Phasers. My first attempt was clunky but functional to me, however could break with the slightest group update or preset change. So kept working on that, testing it on various rock and theatre shows that I was working on. Eventually got it to the stage of stability and not able to break it by changing anything in patch/groups/presets, Using worlds applied to the Phaser Faders and a Single Grid or Linear Select group applied to the Recipe Line and varying forms options controlled by macros.

My Next goal was a more Compact Position Picker with more Position options (Low/Mid/High) as I am often working on a MA 3 Light and wanted to reduce the amount of View changes I needed to make per Change. I also wanted to be able to select a number of position changes per each group and trigger them all at the same time either with a snap or a fade. A similar function to Giaffo Designs 'RateMaster "Go"'.

Trying to create the Color Picker Preset was a fun challenge, having to learn more about the Variables System and using multiple commands per macro line, I still think there are improvements to be made here but think the ones I want like a popup window with the Presets Highlighted for selection will be a Lua Script and perhaps not needed. I did make it that rather than having to type in the Name or Macro Number of the Preset you want to save too you can type the store color preset button and then just select the preset icon on the screen, this is done by leaving the command to store macro number to a variable in the command line, which could be of concern if you get disracted during storing a color preset, and then go to press something else, and it then keeps running the macro. So I think I'll need to create a check or something that the Variable is a Preset within a range. Probably more Lua.

The compacting of the Gobo Selector proved difficult with the implementation of the seperate zoom range across Open/Gobo 1/Gobo 2. While also making it all function with a synced go Button also. Eventually the only way was to seperate out the zoom and focus in the presets, so you have your three zoom levels, and then 14 different Focus Presets (not ideal, hopefully I can find a better way) three each for Open/Gobo 1/Gobo 2 and one each for Iris Small and Animation Wheel.

Hopefully you find this useful either in using the file for your own shows, or finding things in the macros that you can use in your own file! Feel free to link me to any of your gig photos on Instagram or via the Discord #Sscreenshots Channel. I really want to keep building on this, and am open to any suggestions so long as I am capable of doing them!
</details>

### The modifications I have made to the start show are:

* Compact Position Picker, with Go Button to all move at once. (Updated Position Preset Macro, to Include Low/Mid/High Positions.
* Compact Gobo Picker (same page as Positions), with Go Button for Zoom, Focus, Gobo, Animation and Iris Small.
* Color Picker Presets, Find a Color combination you want and save it to a recallable Preset. Create your Color look, and then tap the 'Store Color Preset' button, next tap on one of the 20 Color Preset Buttons on the Layout View then name it.
* Advanced Position Phaser Engine! Two Seperate Phaser Faders, you can Select Which Groups you want to have in the Faders with: Phaser Form, Groups, Blocks, Wings, Phase and Selection Shuffle.
* Advanced Color and Dimmer Phaser Engine! Select which groups you want to have in the Phaser Fader with: Form, XGroups, XBlocks, XWings, Phase and Selection Shuffle.
* Static Color Gradient as part of the Color Picker
* Position Preset Macro asks for you Max Pan and High/Mid/Low Tilt Values.
* Small/Mid/Wide Zoom as a Universal preset. You should just need to save Focus to indicated Presets
* Part of the StartShow Manual Macro now directs you to a Macro that builds your Linear/Even/Odd Groups for you.

### Things Currently on my radar to improve: 

* ~~Part of the Position Preset Macro that asks for your Pan and Tilt Limits (-35 Thru 35 Pan, -10 Thru 100 Tilt Etc.)~~
* ~~A macro that makes your Base Groups (Linear/Odd/Even).~~
* ~~A focus macro that does your (Small/Mid/Wide)~~
* ~~Group Intensity Faders change color depending on what color is set from color picker.~~


# Updates/Fixes

## v0.2.0
* Finalised Gradients Macros, and improved gradient look on color picker.
* Intensity Faders can now follow the color selection for each group with a toggle button on StartShow Content Update layout.
* Modified how the Auto Groups Macro works, to flow better with StartShow File.

## v0.1.9
* Made Color Gradient Universal, Should just work.
* StartShow Manual Macro on StartShow Content Update Layout, now Helps build Half your Groups, and walks you through rest of Setup.
* Postion Maker Macro now asks for you Max Pan Value (e.g. 45), and High/Mid/Low Tilt levels (e.g. 95/45/20) No need for Negative Values, Macro does that for you.

## v0.1.8
* Redesigned the Color Gradient option to use a better system to save having to store into a Magic Preset.
* Trying out some universal Zoom and Iris Presets
* Trying out two Group Creation macros written by Creative Tech Services - <a href="https://www.instagram.com/beamzbeamzbeamz/">@beamzbeamzbeamz</a>

## v0.1.7
* Fixed a bug in the Col/Dim Phaser Form selection that referenced a deleted Sequence, this broke the Form Selection completely.
* Added a Color Gradient to Color Picker, and Foreground/Background Color Selector to bottom of Color Picker

## v0.1.6
* Added a new Dimmer Bump feature seperate from LOS Engine, allowing for simpler 1-shot dimmer bumps. New Layout View called BUMPS saved to MA3 Light/Full-Size Left Screen in Command Section.
* Tidied up appearances and some macros with old references.

## v0.1.5
* Fixed - Bug in the Position and Gobo Layout view, that meant the  "Go" button wasn't respected when switching from delay 0 to any other delay option.
* Fixed - Bug in the Position and Gobo Layout view, that meant the "Go" button wasn't allowing delay movements to complete before resetting and stopping the transition.
* Updated all the Macros on Position and Gobo Layout view to Reference Appearance and Macro's using new system.
* Updated the Custom Input Macros on Position and Gobo Layout view to provide a notification of what it's currently set to once activated, and will show what it was set to previously if changed to 0/2/4/3.

## v0.1.4
* Changed all the Phaser Faders to use the Grid and Linear groups created at the start of showfile creation, simplifying setting up the file and making Blocks and Groups work better within the Phasers. - Deleted Phaser Grid/Linear Groups at 5001+5002.
* Fixed several errors in Macros with incorrect Sequence or Preset Name.
* Fixed the Strict/Normal Macros for each group to work correctly with new Phaser Faders.
* Better indication of what Group/Block/Delay/Fade/OffFade you've set on the Custom Input Button with read out from entered information. - Not yet Implemented on Position/Gobo/Color Picker Layouts, just on Phasers.
* Many more than I can remember it's 1am!

### v0.1.3
* Fixed Color Presets White/CTO/CTB/Red containing Recipe information that wasn't needed.

### v0.1.2
* Finished Position Phaser Phase Invert Macros and Updated Position Phaser Layout view.
* $MAStart_PositionPhaser1XPhaseTo/XPhaseFrom are now defined and controlled by the Phase Invert Macros.

### v0.1.1
* Fixed the Position Phaser 1 macros to correctly set the Position Phaser 1 Variables. 
* Started working on the Position Phaser Invert macros to properly define the $MAStart_PositionPhaser1XPhaseFrom and $MAStart_PositionPhaser1XPhaseTo in the global variables as this doesn't currently exist, except for being manually defined.

### v0.1
* Intial Release


# Usage

You Patch your fixtures the same as the exisiting start show, and build your groups the same. You need your fixtures to be put in their roughly correct 3D position, this makes group creation and the Grid Groups work better with the Phaser Faders.

### Color Gradient Example - Only for Showfile version 0.1.7
[![Color Gradient Example](https://github.com/user-attachments/assets/50972813-3ec5-417f-9d55-2d7858adbc9f)](https://youtu.be/kphdg0l2gx8
)

# Support

Head on over to the MA Users Discord for support for this Showfile - <a href="https://discord.gg/bdxy9MtsqY">
    <img src="https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white" alt="Discord Badge"/>
  </a>


# Screenshots

![Position_Gobo Picker](https://github.com/user-attachments/assets/495fab79-e9b8-4a6f-99a5-08c407a681ce)

![Colour Picker](https://github.com/user-attachments/assets/ade0dcb1-5136-4c3f-81d3-2a12e3931108)

![Position Phaser Picker](https://github.com/user-attachments/assets/8976878f-5436-4f99-903b-653fe5366d95)

![DIM_COL Picker](https://github.com/user-attachments/assets/a7c8a6ac-71c8-4216-8788-23c3b9d3d75e)

![Dimmer Bumps](https://github.com/user-attachments/assets/c1163160-9e56-409d-b7ea-604e116873b3)

![StartShow Content Update](https://github.com/user-attachments/assets/5b52e8dc-e0e3-45ee-99f1-7573c91cf65e)

![Fader Page](https://github.com/user-attachments/assets/42fdfc56-72ed-4e43-9706-3cde0db32b73)
