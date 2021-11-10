# DotClk Help & Instructions

Welcome to the help file for the DotClk pinball animation clock.


## DotClk Board

Figure 1 shows the DotClk board that controls the clock.

![DotClk Board](/Images/DotClkBoard.jpg)

*Figure 1 - DotClk Board*

1. Button 1 - Menu / Back

2. Button 2 - Previous / -

3. Button 3 - Next / +

4. Button 4 - Edit / Save

5. Power In - 5v DC

6. Power Out - To LED Matrix Screen

7. Data Out - To LED Matrix Screen
8. Clock Battery - CR2023 for clock backup, keeps time ticking even without clock power

9. Teensy Micro Controller - Computer controller

10. Micro SD - Insert card containing scenes and fonts

11. USB - Allows programming of the Teensy from a PC or MAC

12. Program Switch

## Power Connection
Connect the power supply to the DotClk board 'Power In', as shown in Figure 2.
![Power Connection](/Images/PowerConnection.jpg)

*Figure 2 - Power Connection*

## Frame
The frame supplied with DotClk can be mounted on a wall using the keyhole slot screw holes on the rear of the frame.

The recommended screw type is 8 X 1.5" roundhead.

For frames supplied from 2018 onwards, the screws should be fitted level at 333mm centres.

For frames supplied before 2018, the screws should be fitted level at 553mm centres.

There is a hole to allow the power cable to pass from behind the frame - it is large enough to accept the cable including the bulky EMI collar.
## Buttons
The buttons perform various functions at different stages whilst using the clock:

**Boot Time**


When the clock is switched on (boot time) the following button actions apply:
* Button 1 held and released - Select display type '0'. Type is shown on screen
* Button 2 held and released - Select display type '1'. Type is shown on screen
* Button 4 held and released - Select display test mode. Press button 4 to exit.

**Clock Mode**

When the clock and animations are being shown:
* Button 1 - Enter menu mode
* Button 4 - Switch off the display. Press button 4 to switch on the display.

**Menu Mode**

After pressing Button 1 in Clock Mode, Menu Mode will be selected:
* Button 1 - Exit from Menu Mode or current menu setting. Current menu setting changes will not be saved
* Button 2 - Move to previous menu item or adjust current menu setting
* Button 3 - Move to next menu item or adjust current menu setting
* Button 4 - Select menu item or save current menu setting

During Menu Mode the screen shows the action of each button at the bottom of the screen.

## Menu Mode

Menu items allow setting of the following features:
* Set Time - Set the hour and minutes. At the point of selecting Save the time is stored with seconds set to zero
* Daylight Saving Time - Easily add / subtract an hour
* Sleep Time - Set a time when the display should go off. If Sleep and Wake time are the same then the clock will stay on
* Wake Time - Set a time when the display should come on. If Sleep and Wake time are the same then the clock will stay on
* Brightness - Adjust the brightness of the dots
* Clock Delay - How many seconds / minutes before displaying an animation
* Clock Font - Choose a font to use for the clock. Anybody can create a new font using the Font Editor tool - simply copy the file into the Fonts directory on the SD Card and choose from this menu.
* Dot Colour - For multi colour displays choose from Red, Green, Yellow, Blue, Cyan, Magenta or White
* Button Mapping - Swap the menu buttons around. Useful if the control board is mounted upside down
* Show Brand - Choose to repeatedly show a selected animation called brand.scn. Use the Scene Editor tool to create a custom animation from GIFs
* Debug - Shows the name of the scene file during playback, and also displays the duration of the previous animation

## Animations & Fonts
All animations and fonts are available for downaload. From time to time new animations or fonts will be created.

You can find the files at the following location:
[DotClk Resources](https://github.com/sigmafx/DotClk-Resources)

Instructions on downloading can be found on this page.

It is also possible for anyone to create new animations and fonts. Applications to do this can be found at the following location:
[DotClk Support](https://github.com/sigmafx/DotClk-Support)

Instructions on using the applications can be found on this page.

## New Firmware
New firmware may be made available to add new features or fix any defects.

You can find the files at the following location:
[DotClk Firmware](https://github.com/sigmafx/DotClk)

Instructions on downloading can be found on this page.

## If the clock keeps crashing / screen goes blank
There has been an issue where the clock appears to stop working - the screen remains blank and it is necessary to turn off, then on to restart the clock, although once this has started happening the clock will show a blank screen again after a short while.

This issue has now been fixed - if you are having this problem please follow these steps:
1. Remove the SD card from the clock and delete all files on it. Download the following zip file:
https://github.com/sigmafx/DotClk-Resources/archive/refs/heads/master.zip

Copy the Scenes and Fonts folders to the SD card form the zip file.

2. Update the firmware installed on the clock by using the latest DotClk.ino.TEENSY35.hex file. Download the following zip file:
https://github.com/sigmafx/DotClk/archive/refs/heads/master.zip

You will need to access the file DotClk.ino.TEENSY35.hex in the zip file - copy the file to a location on your computer so you can access it later.

To update the firmware you will need the Teensy Loader Program - please see this page to download the version for your computer:
https://www.pjrc.com/teensy/loader.html
N.B. You will only need the loader program - do not use the blink test files that are shown on this page.

It will be necessary to connect a micro USB cable to the Teensy micro controller in the clock and use the Teensy Loader Program to open the file DotClk.ino.TEENSY35.hex. The firmware update should happen automatically, but it may also be necessary to force the Teensy to accept the firmware update by pressing the Program Switch, marked as item 12 in Figure 1.

3. You can now insert the SD Card into the Teensy, remove the USB cable and connect to the original power supply. If all is well you should see the clock start, showing a version of at least v1.10.

If you are having issues with this process please send an email to dotclk@drpinball.co.uk.
