# DotClk Help & Instructions

Welcome to the help file for the DotClk pinball animation clock.


## DotClk Board

Figure 1 shows the DotClk board that controls the clock.

![DotClk Board](/Images/DotClkBoard.jpg)

*Figure 1*

1. Button 1 - Menu / Back

2. Button 2 - Previous / -

3. Button 3 - Next / +

4. Button 4 - Save

5. Power In - 5v DC

6. Power Out - To LED Matrix Screen

7. Data Out - To LED Matrix Screen
8. Clock Battery - CR2023 for clock backup, keeps timing even without clock power

9. Teensy Micro Controller - Computer controller

10. Micro SD - Insert card containing scenes and fonts

11. USB - Allows programming of the Teensy from a PC or MAC

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
* Button 4 - Switch off the display. Press button 4 to switch on display.

**Menu Mode**

After pressing Button 1 in Clock Mode, Menu Mode will be selected:
* Button 1 - Exit from Menu Mode or current menu setting. Current menu setting changes will not be saved
* Button 2 - Move to previous menu item or adjust current menu setting
* Button 3 - Move to next menu item or adjust current menu setting
* Button 4 - Select menu item or save current menu setting
During Menu Mode the screen shows the action of each button at the bottom of the screen.

## Menu Mode

Menu items allow setting of the following features:
* Set Time
* Daylight Saving Time - Add / sub an hour easily
* Sleep Time - Set a time when the display should go off
* Wake Time - Set a time when the display should come on
If Sleep and Wake time are the same then the clock will stay on

* Brightness - Adjust the brightness of the dots
* Clock Delay - How many seconds / minutes before displaying an animation
* Clock Font - Choose a font to use for the clock
Anybody can create a new font using the Font Editor tool I've written - simply copy the file into the Fonts directory on the SD Card and choose from this menu.

* Dot Colour - For multi colour displays choose from Red, Green, Yellow, Blue, Cyan, Magenta or White
* Button Mapping - Swap the menu buttons around - useful if the control board is mounted upside down
* Show Brand - Choose to repeatedly show a selected animation - could be used by shops and bars to have their brand logo on screen. Currently no means to generate a custom animation, but I'll be updating the Scene Editor tool to allow this
* Debug - Currently shows the name of the scene file during playback, and also displays the duration of the previous animation
